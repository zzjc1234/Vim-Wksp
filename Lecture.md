

# Part 2 -- vimrc

## Without Plugin

See -> `Vim-Wksp/vimrc-noplugin/vimrc`

We strongly suggest you do this:

```
cd ~/
git clone https://github.com/zzjc1234/Vim-Wksp.git
mkdir .vim
cd .vim
cp ~/Vim-Wksp/vimrc-noplugin/vimrc ~/.vim/vimrc
vim
```

Now your vim should be look like this

![](https://raw.githubusercontent.com/Hydraallen/images/master/img/Snipaste_2023-03-29_18-37-16.png)

Next `:q`

And `vim vimrc`

Read it line by line! (cover `split` btw)

### Shortcut key&key mapping

1. `map` Equivalent key

`noremap` Change key 

change`a` into`b`

```
noremap a b
```

Move faster!

```
noremap H 5h
noremap J 5j
noremap K 5k
noremap L 5l
```

Quick save and source

```
map s <nop> 
"s为删掉当前字符并进入写入模式
map S :w<CR> 
"<CR>表示回车，效果：S即保存写入
map Q :wq<CR> 
"效果：Q即退出vim
map R :source R $MYVIMRC<CR> 
"效果：R刷新vimrc
map ; :
```

2. `set`-> see detail in `vimrc-noplugin/vimrc` 

3. split screen

`:spilt` split up and down

In `vimrc-noplugin`,`su` for split up，`sd` for split down

`:vspilt`split left and right

In`vimrc-noplugin`,`sl` for split left `sr`for split right

Move the cursor position manually  `ctrl+w+h/j/k/l`

4. Change backgroud (Do you want to be manuel)

   `:color` +tab

   Go back to default `:color default`

## With Plugin

See -> `Vim-Wksp/vimrc-withplugin/vimrc`

We strongly suggest you do this in wksp:

1. Install [Vundle](https://github.com/VundleVim/Vundle.vim)

```
cd ~/.vim
mkdir bundle
cd bundle
git clone https://github.com/VundleVim/Vundle.vim.git
```

Windows users may need to refer to this ->  https://github.com/VundleVim/Vundle.vim/wiki/Vundle-for-Windows`

2. Write `vimrc`

*You don't need to write now because I have prepared it for you. All you need to do now is to understand!*

```
set nocompatible              " be iMproved, required
filetype off
" set the runtime path to include Vundle and initialize
set rtp+=~/.vim/bundle/Vundle.vim
call vundle#begin('~/.vim/bundle')
" alternatively, pass a path where Vundle should install plugins
"call vundle#begin('~/some/path/here')

" let Vundle manage Vundle, required


call vundle#end() " required

filetype on " required
filetype indent on  " required
filetype plugin on  " required
filetype plugin indent on " required
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
```



3. Find and install plugin

+ Search in Github
+ ![](https://raw.githubusercontent.com/Hydraallen/images/master/img/Snipaste_2023-03-25_01-00-39.png)
+ write in vimrc `Plugin 'vim-airline/vim-airline'`
+ plug install `:PluginInstall`或`:BundleInstall`  
  plug update `:PluginUpdate`  
  plug uninstall `:PluginClean`  

4. Time to have a try!

We strongly suggest you do this in wksp:

```
cd ~/
git clone https://github.com/zzjc1234/Vim-Wksp.git
mkdir .vim
cd .vim
cp ~/Vim-Wksp/vimrc-withplugin/vimrc ~/.vim/vimrc
vim vimrc
```

There will be some warnings or errors. But **DO NOT PANIC**, just press `enter`

![](https://raw.githubusercontent.com/Hydraallen/images/master/img/Snipaste_2023-03-29_19-03-11.png)

Now install some plugin `:PluginInstall`

(In vimrc-withplugin, we included `airline, snazzy,ale,nerdtree`)

![](https://raw.githubusercontent.com/Hydraallen/images/master/img/ezgif.com-video-to-gif.gif)

And now your vim should be look like this:

![](https://raw.githubusercontent.com/Hydraallen/images/master/img/Snipaste_2023-03-29_19-14-15.png)

If you want use more plugin and don't want to spend too much time, you may refer to `Vim-Wksp/vimrc-sample/vimrc`



## Vim Macro

   You can use vim macro to complete the repetition work.

   1. Enter `q\<char\>` to start recording the macro.
   2. Edit one line
   3. Enter `q` to stop recording
   4. Move to the line you modify(You can include this step in recording the macro)
   5. Enter `@\<char\>`

Now exercise!



## Suggestions

1. If you want use vim more smoothly, you may need to change `esc` and `Capslock`

In macOS, you may use karabiner

In WIndows, you may use Powertoys

In Linux, I believe you can find one by yourself!

2. plugin 

Here are some recommendations:

5. 插件list（推荐）

+ [airline ](https://github.com/vim-airline/vim-airline)   状态栏

+ [snazzy](https://github.com/connorholyday/vim-snazzy)  配色

  ```
  colorscheme snazzy
  ```

+ [nerdtree](https://github.com/preservim/nerdtree)   文件树

+ [tagbar](https://github.com/preservim/tagbar)  显示函数列表

+ [ale](https://github.com/dense-analysis/ale)   错误检查

+ [YouCompleteMe](https://github.com/rdnetto/YCM-Generator)    代码自动补全

+ markdown-preview

3.  Cheet Sheet

   https://devhints.io/vim

4. b站 @ TheCW

   https://cloud.tencent.com/developer/column/4987




## Other vim

+ Neovim

NeoVim 项目地址: [GitHub - neovim/neovim](https://link.zhihu.com/?target=https%3A//github.com/neovim/neovim)

Vim 原项目地址: [GitHub - vim/vim](https://link.zhihu.com/?target=https%3A//github.com/vim/vim)

+ [supervim](https://github.com/Linfee/supervim)
+ [lunarvim](https://www.lunarvim.org/zh-Hans/)

有非常详细的官方文档，可以参考`Vim-Wksp/vimrc-sample/lunarvim-config.lua`

+ emacs

![](https://raw.githubusercontent.com/Hydraallen/images/master/img/the_violence_has_escalated.png)

## Throw Away Your Mouse！

+ vscode

  You may refer to -> `Vim-Wksp/vimrc-sample/vimrc-vscode`

  ![](https://raw.githubusercontent.com/Hydraallen/images/master/img/Snipaste_2023-03-30_16-33-50.png)

+ help/man

+ [Ranger](https://github.com/ranger/ranger) -> available for macOS and Linux

​		Use vim key bindings to manage your files

​		You may refer to -> `Vim-Wksp/Usage-reference/ranger.md`

​		(If you use windows with powershell and posh, you can use [lf](	))

+ Use vim key bindings when surffing the Internet
  + [vimium](https://chrome.google.com/webstore/detail/vimium/dbepggeogbaibhgnhhndojpepiihcmeb) -> Google Chrome
  + [vimari](https://apps.apple.com/us/app/vimari/id1480933944?mt=12) -> Safari
  + [vimium c](https://microsoftedge.microsoft.com/addons/detail/vimium-c-%E5%85%A8%E9%94%AE%E7%9B%98%E6%93%8D%E4%BD%9C%E6%B5%8F%E8%A7%88%E5%99%A8/aibcglbfblnogfjhbcmmpobjhnomhcdo) -> edge

You may refer to -> `Vim-Wksp/Usage-reference/vimium.md`

+ [sioyek ](https://sioyek.info/) -> available for macOS, Windows and Linux

  Use vim key bindings to view pdf files

​		You may refer to ->`Vim-Wksp/Usage-reference/sioyek.md`

+ [lazygit](https://github.com/jesseduffield/lazygit)
