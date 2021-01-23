# LLVM Project
llvm程序验证项目进展，讨论总结与计划

## Sample-based model checker 项目每周进展与讨论总结

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

Dafny调研报告: [11.18 Report](https://github.com/fengwz17/LLVM-Project/blob/master/11.18%20Survey%20of%20Dafny%20and%20related%20verification%20tools.pdf)

Dafny相关资料：

1 [Dafny main page](https://www.microsoft.com/en-us/research/project/dafny-a-language-and-program-verifier-for-functional-correctness/)

2 [Dafny github](https://github.com/dafny-lang/dafny);

3 [Dafny online guide](https://rise4fun.com/Dafny/tutorial/Guide);

4 [Dafny reference manual](https://dafny-lang.github.io/dafny/DafnyReferenceManual/DafnyRef);

5 [the Encoding of Dafny to Boogie2](https://www.microsoft.com/en-us/research/uploads/prod/2008/12/Dafny_krml190.pdf).

Boogie:

[This is Boogie2](https://www.microsoft.com/en-us/research/publication/this-is-boogie-2-2/?from=https%3A%2F%2Fresearch.microsoft.com%2Fen-us%2Fum%2Fpeople%2Fleino%2Fpapers%2Fkrml178.pdf).

## [1.5](https://github.com/fengwz17/LLVM-Project/blob/master/1.5.md)

#### llvm框架：

* 调研一些相关工具和sv-comp，汇总资料，特点、优势、不足，我们如何改进；

* 搭建llvm大框架，模块化，可扩展，设计架构，接口；

#### 具体问题

* 找到可以做的具体问题、性质，以之为主线，在框架下开发整合.

## 1.12

### 报告
* Seahorn框架介绍：[1.12 Report](https://github.com/fengwz17/Paper-List/blob/master/1.12_seahorn.pdf);

### 讨论
#### 如何借鉴Seahorn的优点来开发我们的工具：
* 前端的common的技巧实现，对应我们的trace ab..

* 看一下他们怎么做的，怎么加的抽象解释工具？基于trace abtrac...对应到哪里，放在哪个框架里面？在middle end的地方放一个自动机的东西，我们还需要cegar

#### 抽象解释：

* 基于例子，看一下课件，看一下抽象解释怎么算最小不动点，弄清楚怎么转过来的；这里区别是无所谓抽象域，但是，底层编码的思路是很紧密的，都是算不动点

* heap，内存和指针与分离逻辑的关系。

#### 工具的具体实现：
* 具体怎么转到horn子句的？

* 后端: CHC和后端工具到底是啥关系？仔细看一下工具框架。深入调研这个工具。

### 后面的任务
* Symbolic exe文章讲一下

* 调研sv comp的track

## 1.19

### 报告
* SVCOMP调研：[svcomp categories](https://github.com/fengwz17/LLVM-Project/blob/master/1.19_svcomp.pdf).

### 讨论

* 熟悉seahorn，理解里面有意思的技术

* termination文章，跑一下看看benchmark，以了解seahorn为主，后面指定开发计划，idea

* 继续了解ai在seahorn怎么做的，ai工具的POPL文章[(https://doi.org/10.1145/3371082)](https://doi.org/10.1145/3371082) 看一下，考虑对大型程序的指针分析；

* 读rl做程序分析的文章. [(https://doi.org/10.1007/978-3-319-96145-3_12)](https://doi.org/10.1007/978-3-319-96145-3_12)



