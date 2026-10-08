# riptide-plugin-template

A template for [riptide](https://github.com/joshzcold/riptide) plugins. Press
**Use this template**, rename `reading-list` to your plugin's name (the
folder under `lua/`, `name` in `riptide-plugin.toml` and the spec), and
replace the example. As it stands it's a working plugin: save pages to read later with `<Space>r`, and
`:reading-list` shows them.

```lua
-- config.lua
rt.pack.add({ "https://github.com/you/reading-list", opts = { key = "<Space>r" } })
```

## Layout

| Path | |
|---|---|
| `riptide-plugin.toml` | name, description, permissions |
| `lua/reading-list/init.lua` | the module; `setup(opts)` runs when it loads |
| `test/*_spec.lua` | tests, run by `riptide --plugin-test .` |
| `.github/workflows/test.yml` | runs the tests on every push |

`riptide --lua-types > rt.meta.lua` gives lua-language-server the API.
