### 关于 HadoopBuild
> 
> Hadoop在Windos平台上运行的问题。Hadoop在访问本地文件和hdfs文件系统时，需要使用本地库，本地库中使用了Windows的API来实现类posix的文件访问许可。而这个本地库的实现就是Hadoop.dll和winutils.exe。

> 特别是winutils.exe文件，必须放在%HADOOP_HOME%\BIN\目录下。否则Hadoop和使用Hadoop构建的项目无法正常运行。

#### 编译环境：
##### hadoop2.7.7 - hadoop3.1.1
- JDK1.7.0_80/JDK1.8.0_181
- C# Compiler version 4.7.3062.0
- maven 3.6.0
- ProtocolBuffer 2.5.0
- CMake 3.13.2
- VS2010
- mingw-w64 x86_64 8.1.0


> 如果本项目对你有帮助，请点赞支持一下。


### About HadoopBuild
> 
> Problems running Hadoop on Windows. Hadoop requires native libraries on Windows to work properly -that includes to access the file:// filesystem, where Hadoop uses some Windows APIs to implement posix-like file access permissions.This is implemented in HADOOP.DLL and WINUTILS.EXE.
> 
> In particular, %HADOOP_HOME%\BIN\WINUTILS.EXE must be locatable.If it is not, Hadoop or an application built on top of Hadoop will fail.

#### Compile environment：
##### hadoop2.7.7 - hadoop3.1.1
- JDK1.7.0_80/JDK1.8.0_181
- C# Compiler version 4.7.3062.0
- maven 3.6.0
- ProtocolBuffer 2.5.0
- CMake 3.13.2
- VS2010
- mingw-w64 x86_64 8.1.0

>If this project is helpful to you, please support thumb up.

