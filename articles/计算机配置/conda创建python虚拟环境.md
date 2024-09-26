# conda创建python虚拟环境

## 虚拟环境的创建、设置与删除

1. conda创建python虚拟环境

```
conda create -n your_env pythono=3.10
```

这段命令创建一个名为`your_env`的python3.10环境。

2. 激活python虚拟环境

```
conda activate your_env
```

这段代码激活创建的`your_env`环境。

3. 设置清华镜像源

在已激活的`your_env`中输入如下命令：

```
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main/
conda config --set show_channel_urls yes
```

4. 删除虚拟环境

如果想删除`your_env`环境，只需要运行

```
conda remove -n your_env --all
```

即可。

## 解决Jupyter使用不了虚拟环境的问题

只需要安装`ipykernel`即可

```
pip install ipykernel
python -m ipykernel install --user --name=your_env
```