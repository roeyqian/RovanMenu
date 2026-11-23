# Rovan Menu

**Rovan Menu** is a [Windhawk](https://windhawk.net/) mod developed by Roey Qian to customize the Windows 11 Start menu, with a particular focus on its layout, app organization, and menu dimensions.

Designed around the developer's personal preferences, it offers a side-by-side layout, custom app categories, and independent sizing controls for the Start menu and search menu to create a more convenient and personalized Windows experience.

## Features

### Side-by-Side Layout

Reorganizes the Start menu into two panels, keeping the app list and frequently used content accessible at the same time.

- **All Apps:** Keeps the All apps list permanently visible on the left.
- **Pinned and Recommended Items:** Places pinned items, their header, the show more button, and the recommended section in a separately scrolling panel on the right.
- **Layout Adjustments:** Adjusts margins, panel widths, and the navigation and power area to fit the side-by-side arrangement.

**Compatibility:** Uses the redesigned Start menu layout when available and applies a corresponding side-by-side variant on builds that still use the classic Start menu.

### Custom Categories

Custom Categories allow shortcuts in the All apps list to be organized into named groups instead of their original alphabetical groups.

Each category has a name and a list of shortcut names, with the following behavior:

- **Shortcut Matching:** Matches names as displayed in the All apps list, such as `Microsoft Clipchamp`. Matching is case-insensitive.
- **Category Order:** Categories replace letter groups in settings order: the first replaces A, the second replaces B, and so on. Each group's header displays its category name.
- **App Sorting:** Moves matching shortcuts into their category and sorts them by name. Categories with no matching shortcuts are skipped.
- **Remaining Apps:** Moves apps from replaced letter groups to the international group, identified by the globe icon at the end of the list, if they are not assigned to a custom category.

**Category Limit:** Up to 26 categories are supported. Additional categories are ignored.

Category changes are applied live, and disabling the mod restores the original grouping.

### Start Menu Size

Allows the outer dimensions of the Start menu to be configured in pixels, with support for both the classic and redesigned layouts.

- **Width:** Sets the outer width of the Start menu. `0` keeps the default width.
- **Height:** Sets the outer height of the Start menu. `0` keeps the default height.

### Search Menu Size

Provides separate sizing controls for the search menu, allowing it to follow the Start menu dimensions or use its own size.

- **Search Menu Width:** Sets the width in pixels. `0` uses the Start menu width, and `-1` keeps the system default.
- **Search Menu Height:** Sets the height in pixels. `0` uses the Start menu height, and `-1` keeps the system default.

Start menu and search menu size changes are applied live, and disabling the mod restores their original sizes.

## Notes

- The mod customizes the interface at runtime through XAML diagnostics and visual tree watching, without changing system files.
- Interface customization applies to `StartMenuExperienceHost.exe`, `SearchHost.exe`, and `SearchApp.exe`. Custom categories
  only take effect in the Start menu.
- Start menu sizing is applied inside the Start menu process. `explorer.exe` is used only to resize the search menu by
  hooking its positioning code.
- Switching between Start menu layouts automatically restarts the Start menu process once.
- Remote images used by the Start menu are cached, and loading is retried when the network becomes available.
- Only the x86-64 architecture is supported.

## Credits

Rovan Menu is derived from Windows 11 Start Menu Styler, originally developed by [m417z](https://github.com/m417z), and incorporates menu sizing functionality based on the Start Menu Size mod by the same author.

This project builds upon the foundation established by the original mods, introducing a personalized side-by-side layout, custom app categories, and integrated sizing controls for the Windows 11 Start menu and search menu.

Special thanks to m417z for their original work and contributions, which made the development of Rovan Menu possible.

## LICENSE

See [LICENSE](LICENSE) for more information.