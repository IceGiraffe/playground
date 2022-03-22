安装Anaconda小记：
* 首先在官网下载安装包
* 其次是添加环境变量，环境变量需要添加`<installation path>/Library/bin`
* 接着要给conda和pip安装国内源，直接去清华开源镜像站TUNA，里面有改源的tutorial，就别百度如何更换国内源了；
* 如果是Windows，`conda init powershell`，这样可以在PS命令提示符前加一个小括号显示当前的python环境，这是一个全局设置;
* 如果启动PS提示不允许运行脚本，利用管理员权限打开PS然后更改安全设置，`Set-ExecutionPolicy -ExecutionPolicy RemoteSigned`
* 创建新的环境之后，`conda create -n env_name`
  * `conda list`应该是空的，这没问题；
  * 然而，如果此时运行`pip list`，会发现list了一堆包，这其实是base环境安装的包，是没法直接用的；
  * 如果此时在terminal输入python，会提示python解释器是别的环境的，并不是当前环境，上述命令创建的是纯纯的空环境；
  * 所以，创建新环境，应该`conda create -n env_name python=3.9`