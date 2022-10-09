ROS相关指令如果不会自动停止的话，似乎无法触发标准输出信号，`readAllStandardOutput()`函数不能读取输出内容，这里采用`timeout`指令定时终止进程来获取输出，如：
```shell
timeout 5 rostopic hz /turtle1/pose
#5秒后终止rostopic指令。
```