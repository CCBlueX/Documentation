## Text Element
The text element is one of the simplest and yet most important elements of the CustomHUD. On the one hand, it can be used to display static text, but on the other it is also capable of providing additional information about the player, the server and much more. The latter is achieved by using so-called variables. These are replaced with their corresponding value by LiquidBounce in real time. For example, it is possible to display the current coordinates, the ping or the CPS.

#### How to use CustomHUD variables
Below you will find a list of the currently available variables. To use them, either create a new text element or click on an existing one and insert the desired variable.

#### Scaling an element
To change the size of a text element, press and hold the mouse over that element and scroll with your mouse wheel.

### Available Variables
- `%x%` The player's x-position
- `%y%` The player's y-position
- `%z%` The player's z-position
- `%fps%` Current FPS
- `%date%` Today's date
- `%time` Current time
- `%username%` Current Minecraft username
- `%ping%` Your average ping to the server
- `%clientName%` Name of the client (LiquidBounce)
- `%clientVersion%` Build number of the client
- `%clientCreator%` Creator the of client (CCBlueX)
- `%serverIp%` IP of the server you are currently playing on
- `%lcps%` CPS of left mouse button
- `%rcps%` CPS of right mouse button
- `%mcps%` CPS of middle mouse button
- `%cps%` Alias for `%rcps%` 
- `%velocity%` The player's velocity.

#### Example strings
- `Ping: %ping%`
- `X/Y/Z: %x%/%y%/%z%`
- `FPS: %fps%`

![Example]($images$/customhud_variables.png)
