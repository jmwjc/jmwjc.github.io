1. 安装并配置`git`，相关配置可参考[github帮组文档](https://docs.github.com/en/get-started/quickstart/set-up-git)
2. 在终端中键入如下命令克隆项目：
```console
git clone https://github.com/jmwjc/ApproxOperator.jl.git
```
3. 打开`julia`，通过输入`]`或`using Pkg`进入`Pkg`模式，输入如下命令配置项目：
```julia
dev PROJECTPATH
```
其中，`PROJECTPATH`为项目的路径。
4. 在`julia`中输入`using ApproxOperator`即可使用。