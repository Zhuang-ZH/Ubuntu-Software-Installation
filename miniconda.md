主目录创建miniconda目录,下载 Miniconda3 的最新版本安装脚本，并将其保存为 ~/miniconda3/miniconda.sh 文件
```bash
mkdir -p ~/miniconda3
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O ~/miniconda3/miniconda.sh
```

使用bash执行~/miniconda3/miniconda.sh 脚本。  
-b: 表示安装过程中以非交互模式运行，即自动接受默认设置。  
-u: 表示在安装过程中更新已经存在的 Miniconda 程序。  
-p ~/miniconda3: 指定安装 Miniconda 的路径为 ~/miniconda3，即安装到你之前创建的 miniconda3 目录中。  
```bash
bash ~/miniconda3/miniconda.sh -b -u -p ~/miniconda3
```
 删除安装脚本
 ```bash
 rm -rf ~/miniconda3/miniconda.sh
 ```
 安装后，初始化新安装的 Miniconda。以下命令初始化 bash 和 zsh shell：
 ```bash
 ~/miniconda3/bin/conda init bash
 ~/miniconda3/bin/conda init zsh
```

创建新环境
```bash
 # Replace <ENV_NAME> with a name for your environment
 # Replace <PACKAGE> with your desired package
 # Replace <VERSION> with your desired version of Python
 conda create -n <ENV_NAME> python=<VERSION> <PACKAGE>=<VERSION>
```
查看环境信息
```bash
 conda info --envs
```

激活环境
```bash
# Replace <ENV_NAME> with the name of the environment you want to switch to
conda activate <ENV_NAME>
```

退出环境
```bash
conda deactivate
```