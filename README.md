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

后来，更是利用 librime 的「多翻译器协同」，在输入界面内造词，实现了「引导造词」。

![精准造词](https://raw.githubusercontent.com/cppxiaozhu/00/main/aa4.png)
