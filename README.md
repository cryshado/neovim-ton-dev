## neovim-ton-dev

1. Install [neovim](https://github.com/neovim/neovim/wiki/Installing-Neovim)

2. Install [vim-plug](https://github.com/junegunn/vim-plug#neovim)

3. Clone the FunC language support repository into the `parsers` directory in your home directory:
``` 
cd ~ && mkdir parsers && cd parsers && git clone https://github.com/akifoq/tree-sitter-func.git
```

4. Install dependencies (`Node JS` and `npm` must be installed before):
```
cd tree-sitter-func & npm i
```

5. Add current `node_modules` to `PATH`:
```
export PATH=$PATH:./node_modules/.bin
```

6. Just run this:
```
tree-sitter generate
```

7. Create link to queries
```
ln -s /root/parsers/tree-sitter-func/queries /root/.config/nvim/queries/func
```

8. Clone this repository:
```
https://github.com/PythoNyashka/neovim-ton-dev.git
```

9. Copy the configuration files to nvim config directory:
```
cp *.vim *.lua ~/.config/nvim/
```

10. Run `nvim` and execute `:PlugInstall`, then reopen nvim and execute `:TSInstall func`

11. Exit from `nvim` and try to open any `*.fc` file

