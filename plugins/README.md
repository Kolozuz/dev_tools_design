## The what

dev_tools is suposed to be a toolbox for developers, naturally, each user should be able to determine their set of tools depending on their use case, meaning that users should be able to easily manage different tools (add, remove and update them), this means that tools would essentially plugins and we would need a plugin management functionality, said functionality I have in mind is inspired by plugin managers for Neovim such as lazy.nvim.

## The how
For this project, the so called "plugins" would be nothing but Python modules that get imported programmaticaly. As it is the case with plugins made for Neovim, a plugin is hosted in a github repository, and, a configuration file will tell dev_tools which plugins to download as well as configs specific to the plugin, here's how a lazy.nvim's config file looks like for reference:
```lua
{
  'stevearc/conform.nvim', -- tells lazy.nvim to install the plugin hosted at "github.com/stevearc/conform.nvim"
  opts = {}, -- passes no options
}
```
The type of configuration file that dev_tools will use is TBD but prolly will go with `.lua` or `.yaml`, regardless, it should be possible to manage plugins directly from the UI.
