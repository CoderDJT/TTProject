# .net core mvc 项目打包成可执行文件

> ##  一 前言
>
> .NET Core 3.0中新增加了一个特性：Publishing Single EXEs，可以通过dotnet publish 命令将整个.net core应用发布为一个可执行文件。
>
> ## 二 准备
>
> ### 使用VS 2019新创建一个MVC项目
>
> 
>
> <img src="resources\img\fdfb2eb5-2ae1-4e7d-9415-59cfe1beda4e.png" alt="fdfb2eb5-2ae1-4e7d-9415-59cfe1beda4e" style="zoom: 80%;" />
>
> ### 然后使用dotnet publish命令发布：
>
> ```c#
> dotnet publish
> ```
>
> ![724dc668-d341-43c2-8eff-6a5b91eb3c82](resources\img\724dc668-d341-43c2-8eff-6a5b91eb3c82.png)
>
> ### 发布后的文件
>
> ![be17aba6-a8f2-475f-8a41-3b5045bfb666](resources\img\be17aba6-a8f2-475f-8a41-3b5045bfb666.png)
>
> #### 可以看到发布之后有很多文件。接下来我们发布成单个可执行文件
>
> * ##  Windows上的发布命令 
>
>   在Windows系统上面执行如下的发布命令
>
>   ```
>   dotnet publish -r win10-x64 /p:PublishSingleFile=true
>   ```
>
>   如下图所示：
>
>   ![b93ff4f5-ee97-4850-b93f-a00dd2911377](resources\img\b93ff4f5-ee97-4850-b93f-a00dd2911377.png)
>
>   #### 我们在查看发布后的文件
>
>   
>
> * ![07a62084-83ac-45c6-9e78-fbf781dda1a3](resources\img\07a62084-83ac-45c6-9e78-fbf781dda1a3.png)
>
>   #### 可以看到：这次只生成了一个exe文件，文件大小约86M。双击该exe文件就可以运行程序：
>
>   ![94de550f-9e95-4285-9bf3-7da10d633a23](resources\img\94de550f-9e95-4285-9bf3-7da10d633a23.png)
>
>   