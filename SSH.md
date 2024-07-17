## 生成新的SSH密钥对
使用 ssh-keygen 命令来生成新的SSH密钥对。在终端中执行以下命令
```bash
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```
这将会询问您密钥文件的保存路径和文件名。通常情况下，它会提示您将密钥保存在默认的 ~/.ssh 目录中  

生成密钥后，您需要确保私钥文件具有适当的权限，推荐权限为 600 或 400。您可以使用以下命令来设置权限
```bash
chmod 600 ~/.ssh/id_rsa      # 或者
chmod 400 ~/.ssh/id_rsa
```