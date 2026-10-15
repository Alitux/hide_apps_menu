# Hide Apps Menu

Hide the **Apps** menu and the module list from every non-administrator user.

## What it does

This module restricts the following records to the **Administrator** group
(`base.group_system`):

| Record | Type | Purpose |
| --- | --- | --- |
| `base.menu_management` | Menu | Root **Apps** menu |
| `base.menu_apps` | Menu | **Apps** submenu |
| `base.open_module_tree` | Action | Module list (`ir.module.module`) |

Because the underlying action is also restricted, non-administrators cannot
reach the module list even through a direct URL. The result: only
administrators see and use the Apps menu.

The restriction is applied through a data file, so it is re-applied whenever
the module is updated (`-u hide_apps_menu`).

## Installation

```bash
odoo -d <database> -i hide_apps_menu --stop-after-init --no-http
```

## Compatibility

Odoo 19.0

## Author

Alitux — <https://github.com/Alitux>

## License

This module is released under the **GNU General Public License v2.0 (GPL-2.0)**.
See the [LICENSE](LICENSE) file for the full text.
