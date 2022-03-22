* 使用VS Code调试功能需要安装对应语言的插件，如C++就需要安装C++插件。
* 每种语言都需要配置一个JSON文件`launch.json`以支持调试功能
* `launch.json`属性
  * `type`调试器的类型，例如Node.js的调试器是node；C++的调试器是`cppdbg`
  * `name`是调试配置的名字，不重要
  * `request`是调试的模式，launch模式表示启动程序并调试；attach模式表示将程序附加到一个正在运行的进程中进行调试。
* VS Code支持全局的`launch.json`配置，可以在全局的`settings.json`文件中使用`launch`属性设置全局的调试配置。全局配置会被当前文件夹下的`launch.json`文件覆盖。
* 