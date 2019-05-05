## Anaconda 使用常用命令

查看conda版本

```shell
conda --version 或 conda -v
```

查看conda的属性信息	

```shell
conda info
```

更新conda

```shell
conda update conda 
```

查看conda安装的环境

```shell
conda env list
```

查看conda命令帮助信息

```shell
conda create --help
```

创建新的虚拟环境

```shell
conda create --name py37 python=3.7
conda create --name py37 anaconda=4.4.0 python=3.7
#py37表示的是创建的虚拟环境的名字，python=3.7表示创建的虚拟环境使用python版本
```

创建新的虚拟环境到指定的文件夹

```shell
conda create --prefix=D:\program\pyenv\py37 python=3.7
conda create --prefix=D:progam\pyenv\py37 anaconda=4.4.0 python=3.7
```

激活新的环境

```shell
Windows：activate py37
Linux,macOS:source activate py37
```

激活指定路径中的环境

```shell
Windows：activte D:\program\pyenv\py37
linux，macOS：source activate D:\program\pyenv\py37
```

查看已经安装的包

```shell
conda list
```

使用conda安装python包

```shell
conda install pkg
#pkg表示想要安装的python包名
```

更新包以及更新所有包

```shell
conda update pkg
conda upgrade --all
```

卸载包

```shell
conda remove pkg
```

搜索包

```shell
conda search search_pkgname
```

安装特定的channel里的包

```shell
conda insatll -c some-channel packagename
```

离开环境

```shell
Windows：deactivate
linux，macOS：source deactivate
```

导出环境

```shell
conda env export > environment.yml
以及
pip freeze >environment.txt
```

导入环境

```shell
conda env create -f environment.yml
或
pip install -r /path/environment.txt
#注意两种方式实现同样的效果，如果其中一种安装不上某一个包，那么就尝试另外一种的安装方式，推荐使用conda安装
```

导出环境到指定的文件夹

```shell
conda env create -f --prefix=D:\program\pyenv environment.yml
```

删除环境

```shell
conda env remove --name envnamr
```

删除指定路径的环境

```shell
conda remove --prefix=D:\program\pyenv]py37 --all
```

























