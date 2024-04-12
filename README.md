在macOS系统中使用Homebrew部署MongoDB是一个相对简单且推荐的方法。以下是一个详细的步骤指南，帮助你在本地环境中成功安装和配置MongoDB。

## 安装前的准备

在开始安装MongoDB之前，确保你的macOS系统已经安装了Homebrew。如果尚未安装，你可以访问Homebrew的官方网站（https://brew.sh/）并按照提供的指令进行安装。

## 安装MongoDB

1. **添加MongoDB的Homebrew仓库**  
   MongoDB提供了一个官方的Homebrew Tap，这使得安装过程更加简便。首先，你需要通过以下命令将其添加到你的Homebrew中：
   ```bash
   brew tap mongodb/brew
   ```
   这一步确保了你能够从MongoDB官方获取到最新版本的MongoDB安装包[1][2][3]。

2. **安装MongoDB社区版**  
   接下来，使用以下命令安装MongoDB社区版。这里以安装版本6.0.1为例，你可以根据需要安装其他版本，只需更改版本号即可。
   ```bash
   brew install mongodb-community@6.0
   ```
   安装过程中，Homebrew会自动下载MongoDB，并完成安装配置[1]。

## 配置和启动MongoDB服务

1. **启动MongoDB服务**  
   MongoDB安装完成后，你可以通过Homebrew服务来启动MongoDB服务器。使用以下命令启动MongoDB服务：
   ```bash
   brew services start mongodb-community@6.0
   ```
   这将以后台服务的形式启动MongoDB服务器[1]。

2. **验证安装**  
   安装并启动服务后，你可以通过运行以下命令来检查MongoDB的版本，以此来验证安装是否成功：
   ```bash
   mongo --version
   ```
   如果安装成功，该命令将显示MongoDB的版本信息[1]。

3. **连接到MongoDB**  
   使用MongoDB Shell（`mongosh`）连接到MongoDB服务器进行测试。在终端中输入以下命令：
   ```bash
   mongosh
   ```
   如果一切正常，你将看到MongoDB Shell的提示符，这意味着你已成功连接到MongoDB服务器[1]。

## 停止MongoDB服务

当你完成MongoDB的使用后，可以通过以下命令停止MongoDB服务：
```bash
brew services stop mongodb-community@6.0
```
这将停止MongoDB服务器，释放相关资源[1]。

## 总结

通过上述步骤，你可以在macOS系统中使用Homebrew轻松地安装和配置MongoDB。这种方法不仅简化了安装过程，而且还便于管理MongoDB服务的启动和停止。如果在安装过程中遇到任何问题，可以参考MongoDB的官方文档或搜索相关的教程和问题解决方案。

Citations:
[1] https://blog.csdn.net/u010008354/article/details/126873086
[2] https://www.runoob.com/mongodb/mongodb-osx-install.html
[3] https://docs.mongoing.com/install-mongodb/install-mongodb-community-edition/install-on-macos
[4] https://juejin.cn/post/7052585815037673479
[5] https://cloud.tencent.com/developer/article/2180821
[6] https://blog.csdn.net/qq_41758969/article/details/125033395
[7] https://juejin.cn/post/6844903910323257352
[8] https://jb51.net/article/93975.htm
