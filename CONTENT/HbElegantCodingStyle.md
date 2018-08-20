# Collection of Elegant Coding Style

~ 持续汇总优雅的代码、码代码姿势，减少给自己找事：

## 开发习惯

### Code a little, run a little, fix a little.

> Make sure parts of your programs work as you work on them. Do not write massive files of code before you try to run them. Code a little, run a little, fix a little.——《Learn Python The Hard Way》

即写完一部分代码就及时运行检查，确认这部分代码是否实现了目标，而非等所有都写完了才运行。

那如何确保实现了目标？测试。例如：需要批量处理多个 csv 文档中的数据，可先输入一个经典的目标文档测试看下效果，再换几个文档测试，最后批量输入目标文档。

###  [Readme Driven Development](http://tom.preston-werner.com/2010/08/23/readme-driven-development.html) 

### 先把通用的头尾内容写完，搭出框架，再填内容

如编码格式、作者、版本、编辑日期等。

又如写 if else 时，先把整体框架写完，再逐级思考：else 都先用 pass ，暂不处理；把 if 写完后再处理 else 。



## 代码风格

- Python 代码规范：[PEP 8 -- Style Guide for Python Code | Python.org](https://www.python.org/dev/peps/pep-0008/) 
- 思考和开发习惯向 [编程的智慧](http://www.yinwang.org/blog-cn/2015/11/21/programming-philosophy) 靠拢


## CHANGELOG 

- 180716 创建