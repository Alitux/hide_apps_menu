# Hide Apps Menu

Hides the **Apps** menu (and the module list) from every non-administrator user.

## What it does

Applies the **`base.group_system`** group ("Role / Administrator") to:

- the root menu `base.menu_management` (**Apps**),
- the submenu `base.menu_apps` (**Apps**),
- the action `base.open_module_tree` (module list), so it cannot be opened
  through a direct URL either.

As a result, only administrators can see and use the Apps menu.

## Installation

```bash
odoo -d <database> -i hide_apps_menu --stop-after-init --no-http
```

Compatible with Odoo 19.0.
