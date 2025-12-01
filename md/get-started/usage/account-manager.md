# Using the Account Manager

The **Account Manager** allows you to:

- Log in with different account types:
  - **Microsoft**
  - **TheAltening** (thealtening.com)
  - **Cracked (offline)**
  - **Session / Access Token**
- Restore the account you started the game with.
- Quickly switch between saved accounts.

## Opening the Account Manager

You can open the Account Manager directly from the Title screen:

1. Look at the **top-right account panel**.
2. Click the **pen (edit) icon** next to your username.

This opens a window listing all stored accounts, along with buttons to add, edit, or remove them.

## Adding Accounts

Each stored entry appears in a list (often with an icon indicating its type). You can click an entry to log into it.

### Microsoft Login

Use this if you own Minecraft on a Microsoft account.

<video controls src="/images/get-started/account-manager/login-with-microsoft.mp4" style="max-width: 100%; border-radius: 8px;"></video>

1. In the **Account Manager**, click **Add Account** and choose **Microsoft**.
2. In the Microsoft account dialog, click **Link Account**. This will open a browser window with the **Microsoft login page**.
3. Alternatively, click **Copy URL** and paste the link into any browser of your choice.
4. Sign into your **Microsoft account** in the browser and confirm the requested permissions.
5. Once the login succeeds, LiquidBounce will:
   - Add the account to the Account Manager.
   - Show it in the **account list** with your Microsoft username.
6. Click the entry to log into this Microsoft account.

After this, the Title screen’s account panel will show your Microsoft username and indicate that you are logged in via Microsoft.

> If you encounter issues when signing in with **Microsoft** or **Session**, see
> [Fixing issues with the system's hosts file](/docs/fixing-liquidlauncher#fixing-issues-with-the-systems-hosts-file).

### TheAltening Login

Use this if you have alt tokens from **[thealtening.com](https://thealtening.com)**.

1. In the **Account Manager**, click **Add Account** → **TheAltening**.
2. Enter the **token** provided by TheAltening.
3. Confirm to save the account.
4. Select the account from the list to log in.

> Make sure you are using tokens from the official **[thealtening.com](https://thealtening.com)** website to avoid invalid or unsafe accounts.

### Cracked (Offline) Login

Cracked accounts are **offline-mode** accounts that work only on servers with online-mode disabled.

1. In the **Account Manager**, click **Add Account** → **Cracked** (sometimes shown as “Offline”).
2. Enter any **username** you want to use.
3. Confirm to save the account.
4. Select the account from the list to switch to it.

The Title screen now displays the chosen offline username. Remember that most public servers require online-mode accounts and will not accept cracked logins.

### Session / Access Token Login

Session (also known as **access token**) lets you log in using an already obtained Minecraft access token, for example from another launcher or tool.

![Login with Session](/images/get-started/account-manager/login-with-session.png)

1. In the **Account Manager**, click **Add Account** → **Session / Access Token**.
2. Paste your **access token** into the token field.
3. Confirm to save the account and then select it to log in.

> Sessions are usually **temporary**. When Mojang/Microsoft invalidates that token (for example after logout or after some time), you may need to enter a fresh one.

## Restoring the Original Game Account

If you started LiquidBounce while already logged into Minecraft (for example via the official launcher), LiquidBounce keeps track of that **original account** and allows you to restore it with a single click.

If you log into other accounts (Microsoft, TheAltening, Cracked, Session) and later want to return to the account that was active when you launched the game:

1. Open the **Account Manager**.
2. Look at the **bottom left bar** and click the **Restore** button (refresh icon).
3. Your session will switch back to the original account, effectively restoring the login you started the game with.

![Restore Original Account](/images/get-started/account-manager/restore-account.png)

This is useful if you temporarily test alts or cracked accounts but want to safely return to your main account afterwards without manually searching for the original account.

## Quick Account Changer

The **Quick Account Changer** allows you to switch between stored accounts with as few clicks as possible.

### Opening the Quick Account Changer

1. On the Title screen, look at the **top-right account panel**.
2. Click anywhere on the **entire account box** (not the individual arrow or pen icons).
3. A compact overlay opens, showing a **short list of your favorite or most recently used accounts**.

This behavior is demonstrated in the video and screenshot below.

<video controls src="/images/get-started/account-manager/changing-account.mp4" style="max-width: 100%; border-radius: 8px;"></video>

![Changing Account](/images/get-started/account-manager/changing-account.png)

### Switching Accounts Quickly

1. In the Quick Account Changer overlay, click the account you want to use:
   - Microsoft accounts will show their Microsoft username.
   - TheAltening, Cracked, and Session entries will show their respective usernames.
2. The client will:
   - Log out of your current session.
   - Log into the **selected account**.
   - Update the **username** shown in the top-right panel.

The whole process only takes a moment and does not require opening the full Account Manager window.

> Use the full Account Manager to add new accounts or manage many accounts, and use the **Quick Account Changer** for everyday switching between a small set of commonly used accounts.

## Random Cracked Username (Arrow Icon)

The **arrow icon** in the top-right account panel is a shortcut for generating a **random cracked username**:

1. Click the **arrow icon** next to your username on the Title screen.
2. LiquidBounce will automatically:
   - Generate a new random cracked username.
   - Switch your session to this new **offline account**.
3. The account panel updates to show the newly generated username.

This is useful when you quickly need a throwaway cracked username without manually adding a new cracked account in the Account Manager.
