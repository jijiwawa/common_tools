## 拉取脚步
### https://repo.anaconda.com/miniconda/
```shell

wget https://repo.anaconda.com/miniconda/Miniconda3-latest-MacOSX-arm64.sh
```

## 安装
```shell
bash Miniconda3-latest-MacOSX-arm64.sh
```

> Miniconda3 will now be installed into this location:
/Users/a111/miniconda3
>  - Press ENTER to confirm the location
>  - Press CTRL-C to abort the installation
>  - Or specify a different location below



## 常用命令
```shell
source ~/.bash_profile
```

```shell
export PATH=/Users/a111/miniconda3/bin/:${PATH}
```

```shell
conda create -n testenv python=3.10 # 创建一个 pythone 3.1，名字为 testenv
conda env list # 显示所有 conda 环境列表（就能看到刚刚创建的 testenv）
conda activate testenv # 激活 testenv 环境
python --version # 显示 testenv 环境中的 python 版本
conda deactivate # 退出当前 conda 环境

conda create -n testenv python # 安装最新版 python
conda search python # 查询可以创建的 python 版本
conda env remove -n testenv # 删除刚创建的 testenv 环境
```

## 附录
国内conda源
```shell
# 添加清华源的channels
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/conda-forge/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/msys2/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/bioconda/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/menpo/

# 设置搜索时显示通道地址（可选，方便排查源的问题）
conda config --set show_channel_urls yes
```
调整优先级
