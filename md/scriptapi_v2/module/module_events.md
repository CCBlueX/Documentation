## Supported script module events
An event is bound to a certain condition. If this condition is met, the event is triggered and the code in the handler function is executed. Different events are associated with different conditions and therefore fulfill different tasks. A general overview of how to use events can be found [here](/docs/ScriptAPI/Creating%20Modules/Overview). This document lists all available events and their purpose.

The general syntax of an event handler is as follows:
```js
module.on(eventName, function(eventData) {

});
```

### Available events
The following events can be used by script modules.

| Event Name  | Has event data? | Description                                           |
|-------------|-----------------|-------------------------------------------------------|
| enable      | No              | Called when the module is enabled.                    |
| disable     | No              | Called when the module is disabled.                   |
| update      | No              | Called every tick (~20 times/s) if the player exists. |
| motion      | Yes             | Called when the player receives motion.               |
| render2D    | Yes             | Called when the client renders 2D elements.           |
| render3D    | Yes             | Called when the client renders 3D elements.           |
| packet      | Yes             | Called every time a packet is processed.              |
| jump        | Yes             | Called when the player jumps.                         |
| attack      | Yes             | Called when the player attacks an entity.             |
| key         | Yes             | Called when a key is pressed.                         |
| move        | Yes             | Called when the player moves.                         |
| step        | Yes             | Called when step tries to step up a block.            |
| stepConfirm | No              | Called when step successfully stepped up a block.     |
| world       | Yes             | Called when the world is changed.                     |
| session     | No              | Called when the session is changed.                   |
| clickBlock  | Yes             | Called when a block is clicked.                       |
| strafe      | Yes             | Called when the player strafes.                       |
| slowDown    | Yes             | Called when the player is slowed down.                |

### Event data
Many events, when they are triggered, pass some information to the handler function that is relevant to the event. This information is documented below.

#### Motion event

| Method                    | Description          | Type       |
|---------------------------|----------------------|------------|
| eventData.getEventState() | State of this event. | EventState |
EventState can be one of the following:
- PRE
- POST

#### Render2D event

| Method                      | Description                                                                                                                                  | Type   |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|--------|
| eventData.getPartialTicks() | Returns the time passed between the last and the current frame. Can be used to execute animations at the same speed regardless of FPS count. | float  |

#### Render3D event

| Method                      | Description                                                                                                                                  | Type   |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|--------|
| eventData.getPartialTicks() | Returns the time passed between the last and the current frame. Can be used to execute animations at the same speed regardless of FPS count. | float  |

#### Packet event

| Method                | Description                                    | Type   |
|-----------------------|------------------------------------------------|--------|
| eventData.getPacket() | Returns the packet which triggered this event. | Packet |
| event.cancelEvent()   | Cancels the event.                             | void   |
Example:
```js
var C00Handshake = Java.type("net.minecraft.network.handshake.client.C00Handshake");

...

module.on("packet", function(eventData) {
    var packet = eventData.getPacket();

    if (packet instanceof C00Handshake) {
        Chat.print("Cancelling handshake.");
        eventData.cancelEvent();
    }
});
```

#### Jump event

| Method                  | Description                            | Type   |
|-------------------------|----------------------------------------|--------|
| eventData.getMotion()   | Returns the y-motion used for jumping. | float  |
| eventData.cancelEvent() | Cancels the event.                     | void   |

#### Attack event

| Method                      | Description                  | Type   |
|-----------------------------|------------------------------|--------|
| eventData.getTargetEntity() | Returns the attacked entity. | Entity |

#### Key event

| Method             | Description                        | Type |
|--------------------|------------------------------------|------|
| eventData.getKey() | Returns the ID of the pressed key. | int  |
Example:
```js
module.on("key", function(eventData) {
    var key = eventData.getKey();

    if (key == 28) {
        Chat.print("Pressed enter key!");
    }
});
```

#### Move event

| Method                  | Description                                 | Type |
|-------------------------|---------------------------------------------|------|
| eventData.getX()        | Returns the x-position the player moved to. | int  |
| eventData.getY()        | Returns the y-position the player moved to. | int  |
| eventData.getZ()        | Returns the z-position the player moved to. | int  |
| eventData.zero()        | Sets x, y and z position of the event to 0. | void |
| eventData.zeroXZ()      | Sets x and z position of the event to 0.    | void |
| eventData.cancelEvent() | Cancels the event.                          | void |

#### Step event

| Method                    | Description                                                   | Type  |
|---------------------------|---------------------------------------------------------------|-------|
| eventData.getStepHeight() | Returns the height in blocks the client is trying to step up. | float |


#### World event

| Method                     | Description                   | Type        |
|----------------------------|-------------------------------|-------------|
| eventData.getWorldClient() | Returns the new world client. | WorldClient |

#### ClickBlock event

| Method                      | Description                                            | Type       |
|-----------------------------|--------------------------------------------------------|------------|
| eventData.getClickedBlock() | Returns the BlockPos of the clicked block.             | BlockPos   |
| eventData.getEnumFacing()   | Returns the facing state used when clicking the block. | EnumFacing |

#### Strafe event

| Method                  | Description                                                                    | Type  |
|-------------------------|--------------------------------------------------------------------------------|-------|
| eventData.getStrafe()   | Returns the amount by which the player strafed.                                | float |
| eventData.getForward()  | Returns the amount by which the player moved forwards.                         | float |
| eventData.getFriction() | Returns the friction present when strafing (eg. caused by block below player). | float |
| eventData.cancelEvent() | Cancels the event.                                                             | void  |

#### SlowDown event

| Method                 | Description                            | Type  |
|------------------------|----------------------------------------|-------|
| eventData.getStrafe()  | Returns the applied strafe slowdown.   | float |
| eventData.getForward() | Returns the applied forwards slowdown. | float |