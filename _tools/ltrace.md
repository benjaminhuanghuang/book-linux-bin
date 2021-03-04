library trace（ltrace，库追踪）解析共享库，即一个程序的链接信息，并打印出用到的
库函数。

```
ltrace <program> -o program.out
```


查看系统调用
```
  ltrace -S
```
