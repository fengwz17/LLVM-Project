# Sample model checker 项目每周进展与讨论总结

这里简单列出每周进展与讨论总结重点，详细内容见每周文件

### 8.11

开始了解llvm，熟悉llvm IR，阅读与学习llvm pass的写法，一个入门介绍：[LLVM入门引导](https://zhuanlan.zhihu.com/p/122522485)。

### 8.18

#### 进展：

1、继续熟悉llvm，编译并安装clang与llvm，运行了简单的pass样例，熟悉llvm pass的写法；

2、了解了basic block类的基本用法，学习如何编写pass调用basic block的id，遍历前驱后继等。

#### 本周计划：

对简单函数，编写pass获得其CFG。

#### 本周讨论总结：

考虑比较llvm IR不同优化版本的CFG，sampling应用到判断llvm IR优化版本的不同。
