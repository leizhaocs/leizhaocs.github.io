" show line number
set number

" enable hidden buffers
set hidden

" no wrapping
set nowrap

" no swap file
set noswapfile

" set tab to 4 spaces
set tabstop=4 shiftwidth=4 expandtab

" let the color scheme fit dark background
set background=dark

" highlight matched search word
set hlsearch
set incsearch

" disable highlighting the matched parenthesis
let loaded_matchparen=1

" syntax highlight
syntax on

" enable backspace
set backspace=indent,eol,start

""""""""""""""""""""""""""""""""""""""""""""""""""""
" move

" move cursor
nnoremap j h
nnoremap k j
nnoremap l l
nnoremap i k
nnoremap <space> M

" scroll up and down
nnoremap , <c-y>
nnoremap m <c-e>
nnoremap y <c-b>
nnoremap n <c-f>

" move to the beginning and end of line
nnoremap o ^
nnoremap p $

" move to beginning and end of file
nnoremap [ gg
nnoremap ] G

" move word
nnoremap ; b
nnoremap ' w
nnoremap . ge
nnoremap / e

" previous cursor position
nnoremap u <c-o>

" make the same mapping for visual mode
vnoremap j h
vnoremap k j
vnoremap l l
vnoremap i k
vnoremap <space> M
vnoremap , <c-y>
vnoremap m <c-e>
vnoremap y <c-b>
vnoremap n <c-f>
vnoremap o ^
vnoremap p $
vnoremap [ gg
vnoremap ] G
vnoremap ; b
vnoremap ' w
vnoremap . ge
vnoremap / e
vnoremap <space> <c-o>

""""""""""""""""""""""""""""""""""""""""""""""""""""
" insert

" insert relative to cursor
nnoremap s i
nnoremap d a

" insert at beginning and end of line
nnoremap a I
nnoremap f A

" insert new line
nnoremap r O
nnoremap v o

""""""""""""""""""""""""""""""""""""""""""""""""""""
" undo redo

nnoremap ` u
nnoremap \ <c-r>

""""""""""""""""""""""""""""""""""""""""""""""""""""
" delete

" delete current word
nnoremap w daw

" delete current line
nnoremap e "_dd

""""""""""""""""""""""""""""""""""""""""""""""""""""
" copy paste

" visual mode
nnoremap z v
nnoremap zz V

" copy and cut
vnoremap x y
vnoremap c d

" copy and cut a line
nnoremap xx yy
nnoremap cc dd

" paste before to cursor
nnoremap x P
nnoremap c p

"""""""""""""""""""""""""""""""""""""""""""""""""""
" file

" save file
nnoremap q :w<cr>

"""""""""""""""""""""""""""""""""""""""""""""""""""
" find and search

" search pattern
nnoremap t /

" search current word under cursor
nnoremap tt <kMultiply>

" previous and next
nnoremap g N
nnoremap h n

"""""""""""""""""""""""""""""""""""""""""""""""""""
" tab

" switch to explorer
nnoremap <tab> <c-w>w

"""""""""""""""""""""""""""""""""""""""""""""""""""
" fern

" switch to explorer
nnoremap <tab> <c-w>w

" open and close fern
nnoremap b :Fern . -drawer -toggle -reveal=% <cr>

let g:fern#disable_default_mappings = 1

augroup fern_setup
    autocmd!
    autocmd VimEnter * ++nested Fern . -drawer -toggle -reveal=% -width=25
    autocmd filetype fern call FernInit()
augroup END

function! FernInit()
    set nonumber
    nmap <buffer><expr>
        \ <Plug>(fern-my-open-expand-collapse)
        \ fern#smart#leaf(
        \   "\<Plug>(fern-action-open:select)",
        \   "\<Plug>(fern-action-expand)",
        \   "\<Plug>(fern-action-collapse)",
        \ )
    nmap <buffer> <enter> <Plug>(fern-my-open-expand-collapse)
    nmap <buffer> - <Plug>(fern-action-leave)
    nmap <buffer> = <Plug>(fern-action-enter)
endfunction

