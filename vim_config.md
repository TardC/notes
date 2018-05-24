# Vim 实用配置

用户个人的 Vim 配置文件一般是用户**家目录**下的 **.vimrc** 文件，新建该文件并将相关配置写入后重启 Vim 就可以了。下面是一些最常用的配置：
``` Vim
" 不使用vi的键盘模式，而是Vim自己的
set nocompatible
" 语法高亮
syntax on
" 显示行号
set number
" 配色
colorscheme torte
" 设置背景色，每种配色有两种方案，light 或 dark
set background=light
" tab 宽度为4个空格
set tabstop=4
" tab 展开为空格
set expandtab
" 默认缩进4个空格
set shiftwidth=4
" 方便在开启了 expandtab 后使用退格键
set softtabstop=4
" 设置缩进有三个取值：cindent（C风格）、smartindent（智能模式）、autoindent（简单地与上一行保持一致）
set autoindent
```
