
要将.data 节从一个ELF 目标文件复制到另一个文件中
```
objcopy –only-section=.data <infile> <outfile>
```