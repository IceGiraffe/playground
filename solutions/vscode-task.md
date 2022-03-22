* 许多工具都可以把重复的任务自动化，包括代码静态检查、编译、打包、测试、部署等，具体的例子如下所示。
  * 编译：TypeScript编译器、Java编译器等。
  * 静态检查：ESLint、TSLint等。
  * 代码构建：Make、Ant、Gulp、Jake、Rake、MSBuild等。
* 以上这些工具在软件开发周期（编辑、编译、测试和调试）中都是十分常用的工具。所以，为了能更好地和这些工具集成，Visual Studio Code的Task（任务）应运而生。Task可以被用来运行脚本或启动一个进程。因此，许多现有的工具都可以通过Task直接在Visual Studio Code中运行，而不需要额外在命令行中输入命令。Task被配置在.vscode文件夹的tasks.json文件中。
* 注意：Task只能配置在有文件夹打开的项目中。
* 目前还没有使用Task的需求，待有相关需求之后学习补充。