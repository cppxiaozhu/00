## 自成一体的软件包

小狼毫输入法是 Windows 下的中州韵前端，这个大家都很熟悉了。在 RIME 的用户群中，98五笔用户是非常特别的，他们这个社群在 RIME 可被形码利用的范围内，做了高度集成的打包。

### 拆分显示

最初较为亮眼的功能点是通过 OpenCC 的注解功能，实现了「拆分显示」：

- ctrl + shfit + H = 控制拆分显隐
- ctrl + shfit + J = 控制注解模式
- z 键 引导「临时拼音」，并提示「上屏历史」

![拆分显示](https://raw.githubusercontent.com/cppxiaozhu/00/main/aa1.png)

并且做了「拆分、编码、全拼」三重注解：

![拆分显示](https://raw.githubusercontent.com/cppxiaozhu/00/main/aa2.png)

并在拼音反查中，给予全面的注解：

![拆分显示](https://raw.githubusercontent.com/cppxiaozhu/00/main/aa3.png)

### 精准造词

后来，更是利用 librime 的「多翻译器协同」，在输入界面内造词，实现了「引导造词」。而且，当所造的词被上屏过一次后，就会收录到用户目录下的「userphrase.txt」中，方便归纳整理。

- `引导精准造词

![精准造词](https://raw.githubusercontent.com/cppxiaozhu/00/main/aa4.png)

除此之外，还有一些功能如「翻简转换」、「单字模式」、「字符集过滤」等等。在「小狼毫98五笔.exe」这个软件包内部，实现了比较完备的「音形互查」、「拆分助记」、「造词」等五笔刚需。

## 绿色的外挂辅助

### 小狼毫助手

虽然「小狼毫98五笔.exe」这个软件本身挺好用了，但是据我在 QQ 群里的了解，他们仍需向完全没有接触过「RIME」的新手解释一些设置入口与快捷键之类的东西。这种无休止的月经式问题，无休无止，即使有了图文解说，但是 RIME 对于很多新人依然是高不可攀的事物。

后来，社群中「98五笔资源库」的管理制作了「小狼毫助手」，实现了很多功能管理的可视化：

![小狼毫助手](https://raw.githubusercontent.com/cppxiaozhu/00/main/aa5.png)

![小狼毫助手](https://raw.githubusercontent.com/cppxiaozhu/00/main/aa6.png)

![小狼毫助手](https://raw.githubusercontent.com/cppxiaozhu/00/main/aa7.png)

![小狼毫助手](https://raw.githubusercontent.com/cppxiaozhu/00/main/aa8.png)

![小狼毫助手](https://raw.githubusercontent.com/cppxiaozhu/00/main/aa9.png)

虽然实现了的功能很多，但是我觉得最重要的有以下四个：

- 开机辅助唤醒中州韵算法服务

小狼毫开机不可用，算法服务启动缓慢，这个问题很常见，而且佛振一直没有着手解决这个事件。他们通过高权限的任务管理来快速启动「小狼毫助手」，并用助手唤醒「librime」，实现了小狼毫开机即可用的理想状态。

- 中州韵算法服务守护

通过小狼毫助手时时监视「librime」进程，在「librime」意外退出时，即时「重新唤醒」。解决了某些情形下 librime 闪退的问题。

- 主题、方案切换

虽然小狼毫内置了 weasel 主题与输入法方案切换，但是 win10 ，win11 下找那个入口，让很多人无从下手……有些人不知道 win 键可以唤起主菜单、有些人不会用鼠标在托盘里弹右键菜单，而且提这种问题的人，相当多，QQ 群里的管理员常常被这类问题问到崩溃。

- 候选框横竖排切换

这个在之前，是需要改代码才可以的。

### 中州韵助手

虽然「小狼毫助手」解决了一部分设置问题，但是有些用 Mac 和 Linux 的用户常常提类似设置的问题。「98五笔资源库」的管理员经常在 QQ 群里教别人使用 vscode 或 notepad3 之类的工具打开「yaml」，而不是用 windows 内置的「记事本」。可能他们也觉得这不是办法，于是决心自己写一个：要性能好，要跨平台。

![中州韵助手](https://raw.githubusercontent.com/cppxiaozhu/00/main/8.png)

![中州韵助手](https://raw.githubusercontent.com/cppxiaozhu/00/main/2.png)

![中州韵助手](https://raw.githubusercontent.com/cppxiaozhu/00/main/3.png)

![中州韵助手](https://raw.githubusercontent.com/cppxiaozhu/00/main/4.png)

![中州韵助手](https://raw.githubusercontent.com/cppxiaozhu/00/main/5.png)

![中州韵助手](https://raw.githubusercontent.com/cppxiaozhu/00/main/6.png)

![中州韵助手](https://raw.githubusercontent.com/cppxiaozhu/00/main/7.png)
