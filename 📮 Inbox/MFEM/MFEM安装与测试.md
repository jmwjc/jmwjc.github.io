参照安装说明文件(./INSTALL)编译源文件，并生成libmfem.a文件。复制libmfem.a和./include/文件夹至项目根目录，具体命令可参考：
```
cp libmfem.a ${project};cp include ${project}
```
其中，``${project}``为目标项目根目录。
同时，在CMakelist.txt文件中添加下列命令：
```
target_link_libraries(${target_name} libmfem.a)
```
``${target_name}``为目标名。