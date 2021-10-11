# [coc.nvim](https://github.com/neoclide/coc.nvim/wiki/Create-custom-source) 

Coc.nvim is autocomplete plugin for nvim editor, and it allow to create custom source of completion by following two functions:
```
function! coc#source#{name}#init() abort
    return {
        \ 'shortcut': string
        \ 'priority': number
        \ 'filetypes': string
        \ 'firstMatch': string
        \ 'triggerCharacters': string
        \}
endfunction
```
```
function! coc#source#{name}#complete(opt, cb) abort
    let items = ['item1', 'item2', ...]
    call a:cb(items)
endfunction
```
