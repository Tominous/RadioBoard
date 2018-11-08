# RadioBoard
### What is this?
RadioBoard is a Bukkit plugin that uses map items to draw pictures and play GIFs. It is comprised of 2 parts, virtual canvases, and board frames

Virtual canvases are just a blank slate upon which images or shapes can be draw on, and displayed to the player. They can be spread across several board frames, or none at all.

Board frames are in-game structures that are made of a wall with an array of item frames with maps inside of them. Board frames can be of any width or height, and several can be made to show the same Virtual Canvas.

Most of RadioBoard configuration is done through other plugins, or configs. RadioBoard will generate 2 folders by default, one for images and another for display providers. The image folder has the path `/plugins/RadioBoard/images` and the provider folder has the path `/plugins/RadioBoard/providers`. These are where you will place resources that you want to include for your boards. Virtual canvases can be added through the `/plugins/RadioBoard/boards.yml` file.

### Limitations:
Unfortunately, due to Minecraft's packet limit threshold, it is not possible to send an unlimited amount of map packets at the player without the client timing out. Gifs and animations should be limited to roughly 500 full map packets per second. This does *not* mean that the server cannot send out more than 500 packets, simply that any individual player should not receive more than 500 packets per second.

### Usage:
RadioBoard comes with a lot of great core features, such as full dynamic interactive boards that support GIFs, images, buttons, switches, and cool special effects. It also includes a full api for developers.

### Commands:
- `radioboard <board|display|list> ...`
  - `board <create|remove> ...`
    - `board create <name> <map-id>`
      Execute while looking at an item frame to construct a board. The name is unique per board
    - `board remove <name>`
      Remove a board with the given name from existence
  - `display <create|remove> ...`
    - `display create <name> <map-id> <file-name> <x:y>`
      Create a new display based off a template which can be found under /plugins/RadioBoard/providers/
    - `display remove <name>`
      Delete a display forever!(A long time!)
  - `list <boards|displays>`
    View detailed information about all registered boards or displays

### Permissions:
- `radioboard.admin`
  Allows users to run all the commands
- `radioboard.board.<board>.view`
  Allows users to view a default board
- `radioboard.board.<board>.interact`
  Allows users to interact with a default board, assuming they can see it

### Contributors:
- `BananaPuncer714` Creator, Developer
- `Jetp250` Developer