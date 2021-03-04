
system call trace（strace，系统调用追踪）是基于ptrace(2)系统调用的
一款工具，strace 通过在一个循环中使用PTRACE_SYSCALL 请求来显示运
行中程序的系统调用（也称为syscalls）活动相关的信息以及程序执行中捕捉到
的信号量。

跟踪一个程序
```
  strace /bin/ls –o ls.out
```

Attach 到一个现存的进程上
```
  strace –p <pid> -o daemon.out
```

如果想查看读入到文件描述符 3 中的所有数据
```
  strace –e read=3 /bin/ls
```
命令查看写入的数据
```
  strace –e write=fd
```