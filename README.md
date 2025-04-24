update in 2025-04-24
"如果vim启动提示不支持某些插件，启动vim后 :version看下是否支持python3，以及在终端命令行下执行：which vim，确认是用的vim二进制。mac下自带的vim是不支持python的，而且无法更新。"
找到原因：mac终端在启动的时候会优先加载.bash_profile这个文件，而不是.bashrc文件。所以关于vim启动以及 alias等设置需要在.bash_profile中进行修改，或者在.bash_profile文件最后加上：
if [ -f ~/.bashrc ]; then
    source ~/.bashrc
fi


修改了之前的格式错误（启动vim时会提示各种插件用不了，以及编辑的时候显示出错提示）
修改了Normal 模式和插入模式时的 Cursor的形状，方便清晰看到光标下的文字
其他：
如果vim启动提示不支持某些插件，启动vim后 :version看下是否支持python3，以及在终端命令行下执行：which vim，确认是用的vim二进制。mac下自带的vim是不支持python的，而且无法更新。
解决方案：安装一个信的MacVim，在/usr/local/bin下建立 ln -sf /Applications/MacVim.app/Contents/MacOS/Vim /usr/local/bin/vim 软连接，强制是用MacVim
