# vim-mocha

This is a fork from [vim-mocha](https://github.com/geekjuice/vim-mocha).

The current vim-mocha is limited for my personal workflow. 

This fork is intended only for my workflow but will improve it overtime during my development. 

This works with esbuild compiler.

This is a lightweight Mocha runner for Vim. Extracted from
[vim-spec](https://github.com/geekjuice/vim-spec)

Based off of [Attamusc/vim-mocha](https://github.com/Attamusc/vim-mocha) and
subsequently [thoughtbot/vim-rspec](https://github.com/thoughtbot/vim-rspec).


__Use both RSpec and Mocha? Take a look at [vim-spec](https://github.com/geekjuice/vim-spec)!__


## Installation

Using [vundle](https://github.com/gmarik/vundle):

```vim
Bundle 'alarita/vim-mocha'
```

If using zsh on OS X it may be necessary to run move `/etc/zshenv` to `/etc/zshrc`.


Using [pathogen](https://github.com/tpope/vim-pathogen)

```sh
cd ~/.vim/bundle
git clone git://github.com/alarita/vim-spec.git
```

Using [vim-plug](https://github.com/junegunn/vim-plug)

```vim
Plug 'alarita/vim-mocha'
```


## Example of key mappings

__NOTE__: The mappings have changed and use the same mappings as vim-rspec and
vim-spec. If this is a big issue for you, open an issue and I'll re-add/add the
namespace.

```vim
map <Leader>t :call RunCurrentSpecFile()<CR>
map <Leader>s :call RunNearestSpec()<CR>
map <Leader>l :call RunLastSpec()<CR>
map <Leader>a :call RunAllSpecs()<CR>
```

## Configuration

Like [thoughtbot/vim-rspec](https://github.com/thoughtbot/vim-rspec), the
following variables can be overwritten for custom spec commands:

* `g:mocha_js_command`
* `g:mocha_ts_command`

Examples:

```vim
let g:mocha_js_command = "!mocha --recursive --no-colors {spec}"
let g:mocha_ts_command = "!mocha --recursive --no-colors {spec}"
```


Note: [cortado](bin/cortado) is a sugar wrapper for a more complex `mocha` call.


## Notes
* Allow configuration for `mocha` options i.e. `--recursive`, `--reporter dot`

* __BUG__: Last nearest test fails if below `it` call


## Credits

[thoughtbot/vim-rspec](https://github.com/thoughtbot/vim-rspec)

[Attamusc/vim-mocha](https://github.com/Attamusc/vim-mocha)

## License

mocha.vim is released under the [MIT License](LICENSE).
