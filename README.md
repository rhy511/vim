# vim介紹
-------------
- 安裝vim
- 安裝Vundle套件管理器
- 安裝vim color scheme
-------------
## 安裝vim
首先下載vim文字編輯器

```
sudo apt-get install vim
```
查看vim版本

```
vim --version
```

## 安裝Vundle套件管理器
以Vundle套件管理器來來選擇配置，省去用多次make指令來安裝
[下載Vundle](https://github.com/VundleVim/Vundle.vim)

```
git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim
```

自訂vimrc設定檔

```
vim ~/.vimrc
```

建立好vimrc檔案後就可以自行配置
[參考範例](https://www.linuxidc.com/Linux/2017-09/147109.htm)


## 安裝vim color scheme

到Vim網站中下載合適的color scheme.vim
[參考網址](http://vimcolors.com)

建立colors檔案資料夾

```
mkdir ~/.vim/colors
```

將下載好的color schemez.vim放到colors資料夾，以我為例: color scheme = skyhawk，並在vimrc設定檔中加入colorscheme skyhawk

```
mv skyhawk.vim ~/.vim/colors/
vim ~/.vimrc
```

若還有需要額外套件，先下載至本地端，再寫入vimrc設定檔中(使用file + 絕對路徑)

```
Plugin 'file:///home/XXX/.vim/colors/skyhawk.vim'
```

最後進入vim中，並輸入下列指定即可安裝套件

```
:PluginInstall
```

若有些套件需要移除，將vimrc設定檔的套件刪除，並執行下列指令即可移除套件

```
:PluginClean
```

## 問題解決
- 若不太懂linux檔案觀念，可適時在網址列輸入根目錄(/)，查看家目錄(home)下的檔案
- 在運用上述vimrc設定檔範例時，要自行修改需要的套件與對應的color scheme
- 必須在my plugins start條列下加入colorsheme.vim的路徑

## 參考資料
- [從零開始配置你的個性化vim](https://saul-mirone.github.io/2017/06/20/vim-config/#vim-cha-jian-pei-zhi-bu-fen)
- [挑選Vim顏色(color Scheme)](https://blog.longwin.com.tw/2009/03/choose-vim-color-scheme-2009/)
- [Vim配置詳解](https://www.linuxidc.com/Linux/2017-09/147109.htm)
- <http://vimcolors.com>
- <https://github.com/kamykn/skyhawk>

