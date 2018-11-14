Botfathers Desktop API can be used for Windows and Linux desktop automation. The API provides methods to take screenshots and send fake keyboard and mouse input events. On Linux botfather registeres a fake hardware device to send input events, which can't be ignored by programs such as games. The Desktop API, like any other botfather API, is crossplatform. That means you can use the same code to automate both Windows and Linux desktops.

## Table of contents

[TOC]

## Keycodes

Some Desktop API methods require you to provide a `keycode` string as parameter. These are all keycodes supported by botfather:

#### Number keys

- "0"
- "1"
- "2"
- "3"
- "4"
- "5"
- "6"
- "7"
- "8"
- "9"

#### Character keys

- "a"
- "b"
- "c"
- "d"
- "e"
- "f"
- "g"
- "h"
- "i"
- "j"
- "k"
- "l"
- "m"
- "n"
- "o"
- "p"
- "q"
- "r"
- "s"
- "t"
- "u"
- "v"
- "w"
- "x"
- "y"
- "z"

#### F Keys

- "f1"
- "f2"
- "f3"
- "f4"
- "f5"
- "f6"
- "f7"
- "f8"
- "f9"
- "f10"
- "f11"
- "f12"
- "f13"
- "f14"
- "f15"
- "f16"
- "f17"
- "f18"
- "f19"
- "f20"
- "f21"
- "f22"
- "f23"
- "f24"

#### Arrow Keys

- "left"
- "right"
- "up"
- "down"

#### Modifier keys

- "alt"
- "shift"
- "lshift"
- "rshift"
- "control"
- "lcontrol"
- "rcontrol"
- "capital"
- "caps" (alias)
- "capslock" (alias)
- "caps_lock" (alias)
    
#### Special keys

- "space"
- "tab"
- "esc"
- "escape" (alias)
- "backspace"
- "del"
- "delete" (alias)
- "enter"
- "return"

#### Volume keys

- "volup"
- "volumeup" (alias)
- "volume_up" (alias)
- "voldown"
- "volumedown" (alias)
- "volume_down" (alias)

## Desktop API methods

Every bot script may access a global `Desktop` object which provides the following methods.

##### `Desktop.takeScreenshot();`

Takes and returns an screenshot [Image](../image) of the desktop. On multiple monitor setups the screenshot shows all monitors desktops.


##### `Desktop.getSize();`

Returns the [size](../size) of the desktop. The returned size is the same as the size of the image returned by the `.takeScreenshot` method.


##### `Desktop.getRect();`

Returns a [rect](../rect) wrapping the desktop. The rectancle has it's top left corner at 0,0 and the same size returned by the `.getSize` method.


##### `Desktop.leftClick(position);`

- `position` ([Point](../point)): A position on screen measured in pixels

Sends a left mousebutton click event to the given `position` on screen.


##### `Desktop.middleClick(position);`

- `position` ([Point](../point)): A position on screen measured in pixels

Sends a middle mousebutton click event to the given `position` on screen.


##### `Desktop.rightClick(position);`

- `position` ([Point](../point)): A position on screen measured in pixels

Sends a right mousebutton click event to the given `position` on screen.


##### `Desktop.pressKey(keycode);`

- `keycode` (string): The keycode of the key to press

Sends a key hold event to the desktop, followed by a key release event. This is aquivalent to calling `.holdKey` and then `.releaseKey`.

This method is commonly used to fake keyboard input as they would be typed in by a normal user.


##### `Desktop.holdKey(keycode);`

- `keycode` (string): The keycode of the key to hold

Sends a key hold event to the Desktop. This is like holding a key on your keyboard, but not releasing it. - Like when driving in racing games.


##### `Desktop.releaseKey(keycode);`

- `keycode` (string): The keycode of the key to release

Sends a key release event to the Desktop. Use this method to release a key you hold using the `.holdKey` method.


##### `Desktop.warpCursor(position);`

- `position` ([Point](../point)): A position on screen measured in pixels

Places (warps) the mouse cursor to the given `position` on screen.


##### `Desktop.getCursorPosition();`

Returns the cursors current position on screen as a [Point](../point) object. The position is measured in pixels.