# MAED5851
This is a open repository aimed at sharing the Matlab project for Scientific Computation during the Fall semester in 2021..

# vi/vim
## 配置vim编辑器
1. 设置`TAB`键为4字节

+ `vim /etc/vim/vimrc`
+ 在此文件最后输入如下代码：
`set ts=4 #ts = tab space`


2. VIM编辑器显示行号
`set nu`


## gcc编译C程序
### pre-process:
process macro 处理宏定义
### compile:
 将源文件转换成汇编语言文件，`a.c`->`a.o`
### assemble:
<img src="C:\Users\yongjiec\OneDrive - Intel Corporation\Desktop\GCC_CompilationProcess.png" width="615" height="288" border="0" alt="" />

# gcc
使用gcc编译器（compiler）编译C程序
+ `gcc -help` 查看gcc帮助
+ `gcc -v main.c` full details of the compling process
+ `gcc a.c b.c ... -o <file>` Place the output into <file>

## check Linux version
`lsb_release -a #lsb = linux standard base`

# make 工具
自动编译，避免重复编译

## 编写Makefile语法

### 规则格式
```
目标···...: 依赖文件集合···
	命令1
	命令2
	···
	
```
Target···...:Dependencies...
	COMMAND
	...
	
### 变量 $(variables)
`objects = main.o input.o calcu.o`
`main: $(objects)`

### 操作符
`@echo curname:$(curname)` @不打印命令执行过程
`=` 深拷贝 vs `:=` 浅拷贝 vs `?=` 前面又赋值？未赋值使用等号后面的赋值 `+=`追加

### 自动化变量规则
当`%`出现在目标中的时候，目标中`%`所代表的值决定了依赖中的`%`值，使用方法如下：
`%.o:%.c`

$@ |  ss
$% |  
$< |  
$? |  
$^ |  
$+ |  
$* |  


