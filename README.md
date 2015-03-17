# 简介

这是我修改的将 ipython notebook 转成pdf时使用的Latex模板。

修改的部分有：

- 添加了中文支持
- 添加了字体设置
- 添加了自定义作者
- 添加了添加了目录

# 使用方法

将`ctexart.tplx`下载或克隆到你需要转换的 ipython notebook 文件 FILENAME.ipynb 所在的目录下，使用如下命令将 ipython notebook 转换成`.tex`文件。

    :::bash
    ipython nbconvert --to latex FILENAME.ipynb --template ctexart.tplx

再使用`xelatex`命令将生成的`.tex`文件编译成PDF文件。

    :::bash
    xelatex FILENAME.tex

# 注意

模板中的部分内容尤其是字体部分可能需要修改，负责无法顺利编译通过，请参考模板内的注释进行修改。

# 依赖

使用 ipython 的 nbconvert 功能需要pandoc的支持。

编译生成的`.tex`文件需要`xelatex`引擎，推荐安装`TEXLive`发行版。

# 测试环境

在 Python 2.7.9 + IPython 2.1.0 下测试通过。
