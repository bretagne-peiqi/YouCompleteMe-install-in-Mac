### typical example for .vimrc configuring golang

set nocompatible              " be iMproved

set nu

set noswapfile

syntax on

set backspace=indent,eol,start

set tabstop=4

set shiftwidth=4

set completeopt=menu

set expandtab

":colorscheme ron "desert darkblue

set cindent

set rtp+=~/.vim/bundle/vundle/

call vundle#rc()

Bundle 'gmarik/vundle'

Bundle 'Valloric/YouCompleteMe'  

Bundle 'fatih/vim-go'

Bundle 'dgryski/vim-godef'

Bundle 'Blackrush/vim-gocode'

Bundle 'ctrlpvim/ctrlp.vim'

Bundle 'jiangmiao/auto-pairs'

""""""""""""YCM""""""""""""""""""""

let g:ycm_global_ycm_extra_conf = '~/.vim/bundle/YouCompleteMe/third_party/ycmd/cpp/ycm/.ycm_extra_conf.py'

let g:ycm_collect_identifiers_from_tags_files = 1

let g:ycm_seed_identifiers_with_syntax = 1

let g:ycm_confirm_extra_conf = 0

let g:go_fmt_command = "goimports"
let g:go_addtags_transform = "camelcase"
let g:go_highlight_types = 1

"let g:ycm_seed_identifiers_with_syntax=1    
let g:ycm_complete_in_comments = 1
let g:ycm_complete_in_strings = 1
let g:ycm_collect_identifiers_from_comments_and_strings = 0

nnoremap <leader>jd :YcmCompleter GoToDefinitionElseDeclaration<CR> "


syntax on
filetype plugin indent on
