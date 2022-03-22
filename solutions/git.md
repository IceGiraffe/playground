* 安装完毕之后需要设置`user.name`和`user.email`
  * `git config --global user.name "Wang"
  * `git config --global user.email "mail@mail.com"
* 使用clash显示https或者http错误，可以设置使用代理，clash默认使用的clash端口是`7890`
  * `git config --global http.proxy http://127.0.0.1:7890`
  * `git config --global https.proxy http://127.0.0.1:7890`
* git会将config文件保存到`.gitconfig`文件中，git会在git安装目录和用户根目录下搜索配置文件
  * 可以使用`git config --list --show-origin`命令查看各个config来自哪个`.gitconfig`文件。
  