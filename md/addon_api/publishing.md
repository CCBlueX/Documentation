## Publishing

Add-ons reach players through the Marketplace, where they are installed with `.marketplace subscribe <id>` (see [Add-ons](/docs/add-on-api/using-add-ons)). The template's build workflow uploads a new revision whenever a GitHub release is published.

### Creating the add-on

1. Open **Resources** from the account menu on [liquidbounce.net](https://liquidbounce.net/account/resources) and create a **New resource** of type **Add-on**. It then appears under **Your resources** with its ID.

   ![New Add-on](/images/addons/new-addon.png)

   ![Your Resources](/images/addons/resources.png)

2. Generate an **API token** on the same page. It is shown only once, and regenerating it stops the old one from working.

   ![API Token](/images/addons/api-token.png)

3. In the GitHub repository, under **Settings > Secrets and variables > Actions**, add:

   | Kind     | Name                  | Value                   |
   |----------|-----------------------|-------------------------|
   | Variable | `MARKETPLACE_ITEM_ID` | The ID of the add-on    |
   | Secret   | `API_TOKEN`           | The API token           |

Add-ons and scripts the add-on needs go under **Dependencies** on its page under **Resources**. Subscribing to the add-on subscribes to them as well.

### Releasing

The build versions the add-on `<mod_version>+<minecraft>` and names the jar after it, for example `example-addon-1.0.0+26.3.jar` (see [Project Setup](/docs/add-on-api/developers/project-setup#add-on-version)). Tag the release with that version, `v1.0.0+26.3`, and publish it. The workflow builds the add-on, attaches the jar to the release and uploads it to the Marketplace. The tag becomes the revision's version and the release notes its changelog.

- A tag that does not match the jar fails the workflow before anything is attached or uploaded.
- Pre-releases get the jar attached but are not uploaded.
- Without `MARKETPLACE_ITEM_ID`, nothing is uploaded.

To release one version for several Minecraft versions, build it once per Minecraft version and tag each release accordingly, `v1.0.0+26.2` and `v1.0.0+26.3`.

Pushes to `main` publish the build as a GitHub pre-release tagged `snapshot`, which never reaches the Marketplace. Every run, pull requests included, keeps the jars as the workflow artifact `addon`.

### Uploading by hand

An upload is a zip holding exactly one jar at its root, and the jar needs a readable `fabric.mod.json`. The API rejects anything else. The workflow's upload, by hand:

```sh
zip -j addon.zip build/libs/example-addon-1.0.0+26.3.jar

curl --fail-with-body -X POST \
  "https://api.liquidbounce.net/api/v3/marketplace/$ITEM_ID/revisions" \
  -H "Authorization: Bearer $API_TOKEN" \
  -F "file=@addon.zip" \
  --form-string "version=v1.0.0+26.3" \
  --form-string "changelog=First release"
```

`version` is required, `changelog` is optional.

### Review

New revisions wait for a review by the LiquidBounce team before players receive them, unless the account is a trusted publisher. The add-on's page under **Resources** lists every revision with its state, and the team's note on a rejected one. A live revision can be yanked there; players fall back to the newest remaining one that fits their game with their next update.

### Compatibility

Each player receives the most recently uploaded live revision that fits their game, judged by the `depends` in the jar's `fabric.mod.json`:

- `minecraft` has to accept the player's Minecraft version. A revision without a `minecraft` entry fits no game.
- `liquidbounce`, if present, has to accept the player's LiquidBounce version.

The template declares `"minecraft": "~${minecraft_version}"`, the Minecraft version the jar was built against and its patch releases: `~26.3` fits 26.3 and 26.3.1, but not 26.4. A range without an upper bound, such as `>=26.3`, is read the same way. Publish a revision for every Minecraft version the add-on supports.

Subscribing fails while no revision fits the player's game. A player who is already subscribed keeps the subscription when none fits, for example after changing the Minecraft version, and receives the add-on with the first update after a fitting revision is published. Subscribed add-ons are updated at every start of the game and with `.marketplace update`; an installed or updated add-on is loaded on the next start.
