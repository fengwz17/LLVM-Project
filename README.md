# LLVM Project
llvm程序验证项目进展，讨论总结与计划

# Sample-based model checker 项目每周进展与讨论总结

这里简单列出每周进展与讨论总结重点，详细内容见每周文件

## 8.11

开始了解llvm，熟悉llvm IR，阅读与学习llvm pass的写法，一个入门介绍：[LLVM入门引导](https://zhuanlan.zhihu.com/p/122522485)。

## 8.18

#### 进展：

1、继续熟悉llvm，编译并安装clang与llvm，运行了简单的pass样例，熟悉llvm pass的写法；

2、了解了basic block类的基本用法，学习如何编写pass调用basic block的id，遍历前驱后继等。

#### 本周计划：

对简单函数，编写pass获得其CFG。

#### 本周讨论总结：

考虑比较llvm IR不同优化版本的CFG，sampling应用到判断llvm IR优化版本的不同。

## 9.22

考虑 good for sampling 性质，不做乘积。

## 11.3

#### 1、函数调用怎么处理：

Trace abstraction: 支不支持函数调用？调研

SV-benchmark 往年工具怎么处理函数调用的，state-of-art

#### 2、Dafny：
	
熟悉一下：功能，语言，验证的性质
	
##### Boogie：
	
CPA也用boogie，Ultimate Automizer也用boogie
  
性质已经内置到了C的前置后置条件，相当于直接验证了，搞清楚能搞定哪些性质
  
Boogie在它那里是什么角色？
  
搞清楚一些，让我们的工具定位更清楚：研究什么问题，算法，平台

## 11.10

#### 问题：

1、Dafny是怎么做的，是编码成boogie吗？

2、能不能和其他工具的接口结合起来？能否方便地调用？

3、SMACK能做什么？

4、验证框架能否把别人的优点利用起来？

## 11.18

Dafny调研报告:

Dafny相关资料：