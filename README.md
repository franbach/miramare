<p align="center">
  <img src="https://raw.githubusercontent.com/franbach/miramare/master/screen/logo.png" alt="Miramar Vim Theme"/>
</p>

> Ruby on Rails

![Ruby](https://raw.githubusercontent.com/franbach/miramare/master/screen/miramare_ruby.png)

> Html

![Html](https://raw.githubusercontent.com/franbach/miramare/master/screen/miramare_html.png)

> Javascript

![JavaScript](https://raw.githubusercontent.com/franbach/miramare/master/screen/miramare_js.png)

> Sass

![Sass](https://raw.githubusercontent.com/franbach/miramare/master/screen/miramare_scss.png)

## Features

- Dark brownish warm-toned.
- Soft contrast.
- Customizable.
- Rich support for common file types and plugins.

## Installation

### Via Plugin Manager

Take [vim-plug](https://github.com/junegunn/vim-plug) for example:
```vim
Plug 'franbach/miramare'
```
For better syntax highlighting support, please install [sheerun/vim-polyglot](https://github.com/sheerun/vim-polyglot).

### Manually

1. Clone this repository.
2. Copy `/path/to/miramare/colors/miramare.vim` to `~/.vim/colors/miramare.vim`
3. To install [airline](https://github.com/vim-airline/vim-airline) theme, copy `/path/to/miramare/autoload/airline/themes/miramare.vim` to `~/.vim/autoload/airline/themes/miramare.vim`

## Usage

### Vim

Put this in your vimrc:

```vim
" important!!
set termguicolors

" the configuration options should be placed before `colorscheme miramare`
let g:miramare_enable_italic = 1
let g:miramare_disable_italic_comment = 1

colorscheme miramare
```
> See [Configuration](https://github.com/franbach/miramare#configuration) for more options.
>
If you want to apply this color scheme temporarily, run this command in vim(**this may cause color broken**):
```vim
:colorscheme miramare
```
#### Airline

To enable [airline](https://github.com/vim-airline/vim-airline) color scheme, put this in your vimrc:

```vim
let g:airline_theme = 'miramare'
```

To apply it without reloading:
```
:AirlineTheme miramare
```
#### Configuration

**Note:** The configuration options should be placed before `colorscheme miramare` .

- `g:miramare_transparent_background`: Set to `1` to enable transparent background.
  - Available values: `0`, `1`
  - Default value: `0`
- `g:miramare_enable_italic_string`: Set to `1` to enable italic in `String` .
  - Available values: `0`, `1`
  - Default value: `0`
- `g:miramare_disable_italic_comment`: Set to `1` to disable italic in `Comment` .
  - Available values: `0`, `1`
  - Default value: `0`
- `g:miramare_enable_italic`: Set to `1` to italicize keywords. This option is designed to use with fonts that support cursive italic styles, for example [Fira Code iCursive Op](https://github.com/sainnhe/icursive-nerd-font).
  - Available values: `0`, `1`
  - Default value: `0`
- `g:miramare_enable_bold`: Set to `1` to enable bold in `Type`, `Function`, `Constant` .
  - Available values: `0`, `1`
  - Default value: `1`
- `g:miramare_cursor`: Customize the cursor color, only works in GUI clients.
  - Available values: `'auto'`, `'red'`, `'green'`, `'blue'`, `'purple'`
  - Default value: `'auto'`
- `g:miramare_current_word`: Some plugins can highlight the word under current cursor(for example [neoclide/coc-highlight](https://github.com/neoclide/coc-highlight)), you can use this option to control their behavior.
  - Available values: `'bold'`, `'underline'`, `'italic'`, `'grey background'`
  - Default value: `'grey background'` when not in transparent mode, `'bold'` when in transparent mode.

## FAQ

**Q: It doesn't work as expected.**

**A:**

1. This color scheme is mainly designed for true colors, `set termguicolors` is required. Check output of `vim --version`, maybe your vim doesn't support `termguicolors`.
2. Maybe your terminal emulator doesn't support true colors, you can test it using [this script](https://unix.stackexchange.com/questions/404414/print-true-color-24-bit-test-pattern).
3. If you are running vim in tmux, you need to override default true colors of tmux, as tmux cannot display true colors properly: [#1246 How to use true colors in vim under tmux?](https://github.com/tmux/tmux/issues/1246)
4. There are many highlight group links in syntax files while a color scheme may change them, enabling one color scheme based on another color scheme enabled is very likely to cause colors to break. If any color is broken, you can enable the color scheme in your vimrc instead of after vim startup.

**Q: Which font am I using?**

**A:**

1. JetBrains Mono Medium (Patched - Nerd Fonts) [Jetbrains](https://github.com/ryanoasis/nerd-fonts/tree/master/patched-fonts/JetBrainsMono).
2. Enable italic keywords in this color scheme: `let g:miramare_enable_italic = 1`
3. Disable italic comment(optional): `let g:miramare_disable_italic_comment = 1`

## Inspirations

- [gruvbox-material](https://github.com/sainnhe/gruvbox-material)
- [forest-night](https://github.com/sainnhe/forest-night)

#### THANKS

  * Creator of "Forest Night" theme. Used it to figure out how the Vim color schemes work in practise.

## License

[MIT](./LICENSE) © franbach
