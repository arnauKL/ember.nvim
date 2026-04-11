<p align="center">
  <img src="assets/logo.svg" alt="Ember" width="80" />
</p>

<h1 align="center">Ember for Neovim</h1>

<p align="center">
  <em>One vivid coral spark in a sea of warm graphite.</em>
</p>

<p align="center">
  <a href="https://github.com/ember-theme/ember">Palette & Docs</a> ·
  <a href="https://embertheme.com">embertheme.com</a>
</p>

---

<p align="center">
  <img src="assets/banner.png" alt="Ember — Dark, Soft, and Light variants" width="800" />
</p>

## Installation

### lazy.nvim

```lua
{
  "ember-theme/nvim",
  name = "ember",
  priority = 1000,
  config = function()
    require("ember").setup({
      variant = "ember", -- "ember" | "ember-soft" | "ember-light"
    })
    vim.cmd("colorscheme ember")
  end,
}
```

### Local development

```lua
{
  dir = "~/path/to/ember-theme/nvim",
  name = "ember",
  priority = 1000,
  config = function()
    require("ember").setup({ variant = "ember" })
  end,
}
```

Then in your `init.lua`:

```lua
vim.cmd("colorscheme ember")
```

## Variants

| Colorscheme | Background | Description |
|---|---|---|
| `ember` | Dark (L10%) | Default — comfortable 8.5:1 contrast |
| `ember-soft` | Dark (L13%) | Lifted background, softer contrast |
| `ember-light` | Light (L84%) | Warm parchment, darkened accents |

## Configuration

```lua
require("ember").setup({
  variant = "ember", -- default variant
})
```

Switch variants at runtime:

```
:colorscheme ember
:colorscheme ember-soft
:colorscheme ember-light
```

## Plugin support

Built-in highlight coverage for:

- **Treesitter** — all `@capture` groups, all languages
- **LSP** — semantic tokens, diagnostics
- **Telescope** — prompt, results, preview, matching
- **Snacks** — picker, explorer, notifier, dashboard, indent, terminal
- **nvim-cmp / blink.cmp** — item kinds, matching, menu
- **Which-key** — keys, groups, descriptions
- **Gitsigns** — added, changed, deleted signs and line highlights
- **Neo-tree** — file tree, git status, icons
- **indent-blankline** — indent guides and scope
- **mini.nvim** — statusline, tabline, cursorword, jump, notify, pick
- **Noice** — cmdline, confirm, progress
- **Lazy.nvim** — plugin manager UI
- **Lualine** — exported theme via `require("ember.highlights.plugins.lualine").get()`

## License

MIT — Hossam Saraya
