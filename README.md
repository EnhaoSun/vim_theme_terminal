# Terminal_Vim_Theme
Theme set up for terminal and vim

## Terminal
### Xterm
在 .bashrc 添加:
```shell
export TERM=xterm-256color
```

### Ubuntu terminal
下载[solarized theme for GNU ls](https://github.com/seebi/dircolors-solarized)
```shell
git clone git://github.com/seebi/dircolors-solarized.git
```
dircolor-solarized: 选择深色系 dark256：
```shell
cp ~/dircolors-solarized/dircolors.256dark ~/.dircolors
```

接下来下载 Solarized 的 Gnome-Terminal 配色：
```shell
git clone git://github.com/sigurdga/gnome-terminal-colors-solarized.git
```
到该目录下运行配色脚本：

```shell
cd gnome-terminal-colors-solarized
```
可以自由切换深色和浅色。
```shell
./set_dark.sh 或./set_light.sh，
```
或者./solarize 也可切换，比如执行一次是dark，再一次变light。如此交替。



## VIM
### Vundle
先克隆Vundle插件到本地：
```shell
git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim
```
再配置vimrc👇
### vimrc 配置
```
" Theme settings
set number
syntax on
set showmode
set tabstop=4


"""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""
" Vim vundle
set nocompatible              " 这是必需的
filetype off                  " 这是必需的

" 在此设置运行时路径
set rtp+=~/.vim/bundle/Vundle.vim
" vundle初始化
call vundle#begin()
" 或者传递一个 Vundle 安装插件的路径
"call vundle#begin('~/some/path/here')

" 让 Vundle 管理 Vundle, 必须
Plugin 'VundleVim/Vundle.vim'

" 下面是不同支持幅度的例子
" 保持 Plugin 命令 在 vundle#begin 和 end 之间
" plugin 在 GitHub 仓库
Plugin 'tpope/vim-fugitive'
" 来自http://vim-scripts.org/vim/scripts.html的插件
" Plugin 'L9'
" 未托管在GitHub上的Git插件
" Plugin 'git://git.wincent.com/command-t.git'
" 本地机器上的git软件库（即编写自己的插件时）
" Plugin 'file:///home/gmarik/path/to/plugin'
" sparkup vim脚本在名为vim的该软件库子目录下。
" 传递路径，合理设置运行时路径。
Plugin 'rstacruz/sparkup', {'rtp': 'vim/'}
" 安装 L9 并避免名称冲突
" different version somewhere else.
" Plugin 'ascenator/L9', {'name': 'newL9'}
Plugin 'scrooloose/nerdtree'

"每个插件都应该在这一行之前
call vundle#end()            " 这是必需的
filetype plugin indent on    " 这是必需的
" To ignore plugin indent changes, instead use:
"filetype plugin on
"
" Brief help
" :PluginList       - lists configured plugins
" :PluginInstall    - installs plugins; append `!` to update or just :PluginUpdate
" :PluginSearch foo - searches for foo; append `!` to refresh local cache
" :PluginClean      - confirms removal of unused plugins; append `!` to auto-approve removal
"
" see :h vundle for more details or wiki for FAQ
" Put your non-Plugin stuff after this line
"""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""

" Plugin settings
" NERDTree setting
let NERDTreeShowHidden=1
let NERDTreeMinimalUI = 1
let NERDTreeDirArrows = 1
let NERDTreeShowLineNumbers=1
map <C-n> :NERDTreeToggle<CR>
nnoremap <C-h> <C-w>h
nnoremap <C-j> <C-w>j
nnoremap <C-k> <C-w>k
nnoremap <C-l> <C-w>l
```
