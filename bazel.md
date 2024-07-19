参考网址：
>https://bazel.build/install/bazelisk?hl=zh-cn  

# Bazelisk
建议使用 Bazelisk(A user-friendly launcher for Bazel) 在 Ubuntu、Windows 和 macOS 上安装 Bazel。它会自动下载并安装相应版本的 Bazel。如果您需要根据当前工作目录在不同版本的 Bazel 之间切换，或者需要始终将 Bazel 更新到最新版本，请使用 Bazelisk。

Bazelisk网址：
>https://github.com/bazelbuild/bazelisk?tab=readme-ov-file  

发布页找到bazelisk-linux-amd64下载，https://github.com/bazelbuild/bazelisk/releases  
下载完成后，需要为下载的文件添加执行权限。可以使用 chmod 命令来设置
```bash
chmod +x bazelisk-linux-amd64
```
将 bazelisk-linux-amd64 文件移动到系统的可执行文件路径中,这样做可以让 bazelisk 成为全局可执行命令，可以从任何位置直接运行
```bash
sudo mv bazelisk-linux-amd64 /usr/local/bin/bazelisk
```
由于后续make drake的时候使用bazelisk会导致make出错，所以安装bazel


# Bazel
github上下载bazel-version-installer-linux-x86_64.sh 的 Bazel 二进制安装程序
>https://github.com/bazelbuild/bazel/releases

```bash
chmod +x bazel-version-installer-linux-x86_64.sh
./bazel-version-installer-linux-x86_64.sh --user
```
Bazel 可执行文件会安装到 $HOME/bin 目录中,将此目录添加到默认路径
```bash
export PATH="$PATH:$HOME/bin"
```