* 安装`Remote-SSH`以实现远程开发。
* 如果远程服务器无法安装插件，可以在本机下载VSIX插件安装包，然后连接远程后选择从VSIX安装插件；这样VS Code应该会将本地文件传输到Code Server，然后就Server端从服务器安装。
* 建议使用ssh-keygen工具实现免密登录
  * 使用`ssh-keygen -b 4096 -t rsa`生成一堆密钥；
  * 连接服务器，将`id_rsa.pub`文件夹中的公钥复制到服务器端的`~/.ssh/authorized_keys`文件中即可
* 远程与本地的插件
  * 在SSH远程开发环境中，VS Code的插件运行在两个地方：本地机器和远程SSH主机。与VS C界面相关的（如主题、代码片段）等会运行在本地，其他大多数插件会运行在远程SSH主机。
* 如果有什么问题，可以打开命令面板试试`Remote-SSH`相关的kill命令；实在不行建议试试`Uninstall VS Code Server from host`