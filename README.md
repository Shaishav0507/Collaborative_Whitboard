## Demowhiteboard

[HERE](https://cloud13.de/testwhiteboard/) (Reset every night)

### Without Docker

1. install the latest NodeJs (version >= 12)
2. Clone the app
3. Run `npm ci` inside the folder
4. Run `npm run start:prod`
5. Surf to http://localhost:8080

## Default keyboard shortcuts

Use keyboard shortcuts to become more productive while using Whiteboard.

They are especially useful if you work with interactive displays such as XP-Pen Artist, Huion Kamvas and Wacom Cintiq. These devices have quick buttons (6-8 buttons and scrolling). By default, the buttons on these displays are mapped to standard Photoshop keyboard shortcuts. Keys can be configured to function effectively in other software.

The following are predefined shortcuts that you can override in the file [./src/js/keybinds.js](./src/js/keybinds.js)

| Result                                                           | Windows and Linux    | macOS                   |
| ---------------------------------------------------------------- | -------------------- | ----------------------- |
| Clear the whiteboard                                             | Ctrl + Shift + Z     | Command + Shift + Z     |
| Undo your last step                                              | Ctrl + Z             | Command + Z             |
| Redo your last undo                                              | Ctrl + Y             | Command + Y             |
| Select an area                                                   | Ctrl + X             | Command + X             |
| Take the mouse                                                   | Ctrl + M             | Command + M             |
| Take the pen                                                     | Ctrl + P             | Command + P             |
| Draw a line                                                      | Ctrl + L             | Command + L             |
| Draw a rectangle                                                 | Ctrl + R             | Command + R             |
| Draw a circle                                                    | Ctrl + C             | Command + C             |
| Toggle between line, rectangle and circle                        | Ctrl + Shift + F     | Command + Shift + F     |
| Toggle between pen and eraser                                    | Ctrl + Shift + X     | Command + Shift + X     |
| Toggle between main clolors (black, blue, green, yellow and red) | Ctrl + Shift + R     | Command + Shift + R     |
| Write text                                                       | Ctrl + A             | Command + A             |
| Take the eraser                                                  | Ctrl + E             | Command + E             |
| Increase thickness                                               | Ctrl + Up Arrow      | Command + Up Arrow      |
| Decrease thickness                                               | Ctrl + Down Arrow    | Command + Down Arrow    |
| Colorpicker                                                      | Ctrl + Shift + C     | Command + Shift + C     |
| Set black color                                                  | Ctrl + Shift + 1     | Command + Shift + 1     |
| Set blue color                                                   | Ctrl + Shift + 2     | Command + Shift + 2     |
| Set green color                                                  | Ctrl + Shift + 3     | Command + Shift + 3     |
| Set yellow color                                                 | Ctrl + Shift + 4     | Command + Shift + 4     |
| Set red color                                                    | Ctrl + Shift + 5     | Command + Shift + 5     |
| Save whiteboard as image                                         | Ctrl + S             | Command + S             |
| Save whiteboard as JSON                                          | Ctrl + Shift + K     | Command + Shift + K     |
| Save whiteboard to WebDav                                        | Ctrl + Shift + I (i) | Command + Shift + I (i) |
| Load saved JSON to whiteboard                                    | Ctrl + Shift + J     | Command + Shift + J     |
| Share whiteboard                                                 | Ctrl + Shift + S     | Command + Shift + S     |
| Hide or show toolbar                                             | Tab                  | Tab                     |
| Move selected object up                                          | Up Arrow             | Up Arrow                |
| Move selected object down                                        | Down Arrow           | Down Arrow              |
| Move selected object left                                        | Left Arrow           | Left Arrow              |
| Move selected object right                                       | Right Arrow          | Right Arrow             |
| Drop object                                                      | Ctrl + Enter         | Command + Enter         |
| Add Image to background                                          | Shift + Enter        | Shift + Enter           |
| Cancel all actions                                               | Escape               | Escape                  |
| Delete selected object                                           | Delete               | Delete                  |
| Use Line tool when pen is active (Not changeable)                | Shift (Hold)         | Shift (Hold)            |



#### REST API

You can fully control the whiteboard through a REST API. Explore and test the API for your server version by surfing to: `[yourRootWhiteboardUrl]/apidoc/index.html`
You can see the API for the Demowhiteboard here: [DemoAPI](https://cloud13.de/testwhiteboard/apidoc/index.html)

Note: This API is pretty new, so be sure to use the latest Whiteboard version.

#### WebDAV (Optional)

This function allows your users to save the whiteboard directly to a webdav server (Nextcloud) as image without downloading it.

To enable set `enableWebdav` to `true` in the [configuration](./config.default.yml).

Then set the same parameter on the client side as well:

<b>Client (With and without docker):</b> `http://YOURIP:8080?webdav=true&whiteboardid=MYID&username=MYNAME`

Refresh the site and You will notice an extra save button in the top panel. Set your WebDav Parameters, and you are good to go!


