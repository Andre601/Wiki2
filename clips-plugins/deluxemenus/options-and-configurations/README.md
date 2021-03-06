---
description: About the plugin's options and configurations
---

<!-- Spigot (related) links -->
[1.8.8]: https://helpch.at/docs/1.8.8/org/bukkit/Material.html
[1.12.2]: https://helpch.at/docs/1.12.2/org/bukkit/Material.html
[1.13.2]: https://helpch.at/docs/1.13.2/org/bukkit/Material.html
[1.14.4]: https://helpch.at/docs/1.14.4/org/bukkit/Material.html
[Latest]: https://hub.spigotmc.org/javadocs/spigot/org/bukkit/Material.html
[Enchantments]: https://hub.spigotmc.org/javadocs/spigot/org/bukkit/enchantments/Enchantment.html
[Colors]: https://hub.spigotmc.org/javadocs/spigot/org/bukkit/DyeColor.html
[Patterns]: https://hub.spigotmc.org/javadocs/spigot/org/bukkit/block/banner/PatternType.html
[Sounds]: https://gist.github.com/Andre601/1ab3b4fabd0010ae241156333491c379

<!-- Plugin links -->
[Vault]: https://www.spigotmc.org/resources/34315/

<!-- Other links -->
[Placeholders]: https://helpch.at/placeholders
[minecraftjson]: https://minecraftjson.com/

# Options & Configurations

**DeluxeMenus** is a highly customizable plugin, it has many options and configurations to give you the ability to change everything you want to make your custom menus that fits your server's layout.  
It has **GUI** options to manage the GUI menu, and **Item** options to manage every single item on the GUI menu.

## Useful links

* [Placeholders]
* Materials
  * [1.8.8]
  * [1.12.2]
  * [1.13.2]
  * [1.14.4]
  * [Latest]
* [Enchantments] (Be aware that some enchantments are not available on some items.)
* [Dye Colors][Colors]
* [Banner Patterns][Patterns]
* [Sound Types][Sounds]

## Values keywords

| Keyword        | Description                                                                                                                                                                               |
| :------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **BOOLEAN**    | Replace this with `true` or `false` (If used with a PlaceholderAPI placeholder, this will be `yes` or `no` instead of `true`/`false` [It's changeable from PlaceholderAPI config file.]). |
| **TEXT**       | Replace this with any text. Check the description to find out if you can use color/formatting codes.                                                                                      |
| **\#**         | Replace this with a number. Check the description to see if there are limits.                                                                                                             |
| **COMMAND**    | Replace this with a command without slash (`/`).                                                                                                                                          |
| **SOUND**      | Replace this with a sound name.                                                                                                                                                           |
| **EXPRESSION** | Replace this with a java/placeholder expression/comparison. See [this](requirements.md) page for more information.                                                                        |

## Actions types

| Tag                         | Description                                                                                            |
| :-------------------------- | :----------------------------------------------------------------------------------------------------- |
| `[player] <command>`        | Executes a command as the player.                                                                      |
| `[console] <command>`       | Executes a command from the console.                                                                   |
| `[commandevent] <command>`  | Executes an unregistered command ad the player.                                                        |
| `[message] <text>`          | Sends a message to the player. You can use [placeholders] and color/format codes here.                 |
| `[openguimenu] <menu-name>` | Opens another GUI from DeluxeMenus.                                                                    |
| `[connect] <server-name>`   | Connects the player to a server on the same BungeeCord.                                                |
| `[close]`                   | Closes the currently opened GUI.                                                                       |
| `[json] <JSON-text>`        | Send a json message to the player. Use [this][minecraftjson] website to easily generate the JSON text. |
| `[refresh]`                 | Refresh items in the current menu view. This updates the shown Items themselves.                       |
| `[broadcastsound] <sound>`  | Broadcast a sound to all players on the server.                                                        |
| `[sound] <sound>`           | Play a sound for the player.                                                                           |
| `[takemoney] <amount>`      | Take a certain amount of money from the player. [Vault] is required for this action to work.           |

### **Action tags**

These tags can be added with the action (e.g. `- '[message] example<delay=20>'`).

| Tag                 | Description                                                                    |
| :------------------ | :----------------------------------------------------------------------------- |
| `<delay=<time>>`    | Executes the action after the specified delay (in ticks, 20 ticks = 1 second). |
| `<chance=<chance>>` | Sets a chance to execute the action.                                           |

## General options

### Debug

> ```yaml
> debug: BOOLEAN
> ```
>
> > **Default value:** `false`

Enables/Disables debug mode.  
Sends debug messages to the console.

### Check updates

> ```yaml
> check_updates: BOOLEAN
> ```
>
> > **Default value:** `true`

Enables/Disables checking new updates for the plugin.  
Notifies any operator if there is an update available.

