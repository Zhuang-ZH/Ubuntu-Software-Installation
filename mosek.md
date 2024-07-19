官网下载mosek

>https://www.mosek.com/downloads/  

命令行安装tar.bz2安装包

```bash
tar -xvf mosektoolslinux64x86.tar.bz2
```

邮件获取mosek许可证mosek.lic文件，并将其移动到mosek文件夹下（最好安装在主目录）  

pip install Mosek安装python API  
bashrc路径中设置Mosek可执行路径
```bash
export MOSEK_ROOT="$HOME/mosek/10.2"
export PATH="/home/zhuang/mosek/10.2/tools/platform/linux64x86/bin:$PATH"
export MOSEKLM_LICENSE_FILE="/home/zhuang/mosek/mosek.lic"

```