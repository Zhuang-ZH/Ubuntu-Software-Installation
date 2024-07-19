申请gurobi学术许可证
>https://www.gurobi.com/academia/academic-program-and-licenses/   

安装参考资料：
> https://support.gurobi.com/hc/en-us/articles/14799677517585-Getting-Started-with-Gurobi-Optimizer  

在https://www.gurobi.com/downloads/gurobi-software/ 下载✖64 linux版软件，并且tar xvfz解压缩，将文件移动到/opt目录下

.bashrc设置环境变量
```bash
# Gurobi Environment variables
export GUROBI_HOME="/opt/gurobi1003/linux64"
export PATH="${PATH}:${GUROBI_HOME}/bin"
export LD_LIBRARY_PATH="${GUROBI_HOME}/lib"
```
命令行输入激活码
```bash
grbgetkey 81d6821b-618b-4158-a474-ebee08523a38
```

使用 chown 命令更改拥有者：如果您是目录的拥有者或具有管理员权限，您可以使用 chown 命令将目录的拥有者更改为您自己，并且调整 /opt/gurobi1103 目录的权限,要确保您的用户（zhuang）对该目录有写权限
```bash
sudo chown -R zhuang:zhuang /opt/gurobi1003
sudo chmod u+w /opt/gurobi1003
```
将gurobi.lic文件放在/opt/gurobi1103目录下

然后使用pip将 Gurobi 安装到您当前活动的 Python 环境中
```bash
python -m pip install gurobipy
```



