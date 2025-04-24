* 修改了之前的格式错误（启动vim时会提示各种插件用不了，以及编辑的时候显示出错提示）
* 修改了Normal 模式和插入模式时的 Cursor的形状，方便清晰看到光标下的文字
* 其他：
* *如果vim启动提示不支持某些插件，启动vim后 :version看下是否支持python3，以及在终端命令行下执行：which vim，确认是用的vim二进制。mac下自带的vim是不支持python的，而且无法更新。
* *解决方案：安装一个信的MacVim，在/usr/local/bin下建立 ln -sf /Applications/MacVim.app/Contents/MacOS/Vim /usr/local/bin/vim 软连接，强制是用MacVim
