
# 优秀实践集：Information Architecture

~ 持续汇总令自己舒坦的 Information Architecture 案例，以便越来越敏感哪种信息架构更优雅。

<!-- START doctoc generated TOC please keep comment here to allow auto update -->node
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->


- [卡片层级的输出工具](#%E5%8D%A1%E7%89%87%E5%B1%82%E7%BA%A7%E7%9A%84%E8%BE%93%E5%87%BA%E5%B7%A5%E5%85%B7)
  - [正面案例](#%E6%AD%A3%E9%9D%A2%E6%A1%88%E4%BE%8B)
  - [反面案例](#%E5%8F%8D%E9%9D%A2%E6%A1%88%E4%BE%8B)
- [主题音频呈现机制](#%E4%B8%BB%E9%A2%98%E9%9F%B3%E9%A2%91%E5%91%88%E7%8E%B0%E6%9C%BA%E5%88%B6)
  - [正面案例](#%E6%AD%A3%E9%9D%A2%E6%A1%88%E4%BE%8B-1)
  - [反面案例](#%E5%8F%8D%E9%9D%A2%E6%A1%88%E4%BE%8B-1)
- [问答机制](#%E9%97%AE%E7%AD%94%E6%9C%BA%E5%88%B6)
  - [正面案例](#%E6%AD%A3%E9%9D%A2%E6%A1%88%E4%BE%8B-2)
  - [反面案例](#%E5%8F%8D%E9%9D%A2%E6%A1%88%E4%BE%8B-2)
- [技能类课程界面](#%E6%8A%80%E8%83%BD%E7%B1%BB%E8%AF%BE%E7%A8%8B%E7%95%8C%E9%9D%A2)
  - [正面案例](#%E6%AD%A3%E9%9D%A2%E6%A1%88%E4%BE%8B-3)
  - [反面案例](#%E5%8F%8D%E9%9D%A2%E6%A1%88%E4%BE%8B-3)
- [CHANGELOG](#changelog)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->


## 卡片层级的输出工具

### 正面案例

何为卡片层级？为什么卡片层级对输出助益颇大？优雅趁手的卡片工具需满足什么要求？[卡片助力输入输出，工具我选 WorkFlowy | ishanshan's blog](https://ishanshan.im/selfedu/HbOutputOwetoWorkFlowy.html) 已说过，这里不赘述。

[WorkFlowy](https://workflowy.com/demo/embed/) 是目前我见过的卡片级别工具里最优雅趁手。究其核心奥秘，私以为是其只有唯一「实体」 `node` ，能自如缩进、拖动、折叠展开的 `node` ，简洁却可供性无穷。用户可以自由定义各 `node` 在整个体系中的关系/作用，随时自如调整，不必被文件形态强行划分信息组块。这实在契合信息在脑中的状态。

### 反面案例

国内有团队仿照 WorkFlowy 开发了一款类似的工具 「幕布」，增加各种复杂功能。

坦白说就目前幕布的信息架构来看，我不推荐用它：卡片层级，它太复杂；文件层级，各场景多有比它更优雅的交付方式。

最致命的是，进去之后先创建文件/文件夹，再创建各节点：

![sampleia_mubu.jpeg](http://ishanshan.zoomquiet.top/share/sampleia_mubu.jpeg?imageView2/2/w/400)

这完全违背上述奥秘，也违背卡片层级需要方便移动、组合的根本诉求：写卡片写卡片，目的自在输出更高层级的作品，需易**整合**才宜创造。

且这还带来一个负面影响：难以全文件检索，只能进入单个文件检索。即使未来实现，也定不如 WorkFlowy 的检索效果那般优雅：能呈现当前位置以下、目标字段的所有父层级 node ，便于了然全局——


![sample_workflowy_search.png](http://openmindclub.zoomquiet.top/ishanshan/sample_workflowy_search.png)


## 主题音频呈现机制

### 正面案例

音频属个人输入来源，最好能实现这样的效果：

- 进入音频界面 **10-30s ** 就能判断这些音频是否值得继续听
- 还能快速取用自己需要的信息，提升输入效率

由此，最好满足以下条件：

- 能查看提要图文
- 能便捷地了解各小节讲什么、快速选择收听
- 能倍速播放
- 能便捷地提问交流
- 能方便地查阅相关主题的音频

「在行一点」这个平台基本满足上述条件：

	
![strategyibrainlecture005.png](http://pics.ibrainbaby.cn/share/strategyibrainlecture005.png?imageslim)

### 反面案例

- 模仿微信群语音，每条不超过 60s 的机制，还无法倍速播放，信息获取效率超低。这样的产品太多，不点名了。
- 7 分钟以上的长音频，还不能倍速播放的最容易让人不耐烦。

## 问答机制

线上高效解决问题的问答机制，目前体验较多的是在线问诊，以此举例：




### 正面案例

规则：问诊按次收费，每次问诊可在提问后 24 小时内追问 2 次。比如「丁香医生」。

效果：医患双方都会在每次对话中提供尽可能详细、无歧义的信息，毕竟顶多交互 3 回。双方 ROI 都高。

### 反面案例 

规则：问诊按次收费，付费后 24 小时为问诊时间，IM 形式无限次交流。比如「春雨医生」。

效果：交互无限次，双方 ROI 都低。虽然 IM 形式是大伙儿最习惯的交互形式，这种形态用于解决问题真的很低效。比如我的问诊案例：[「春雨医生」](http://ishanshan.zoomquiet.top/share/sampleia_qa_dr.chunyu.jpeg?imageslim)VS[「丁香医生」](http://ishanshan.zoomquiet.top/share/sampleia_qa_dr.dingxiang.jpeg?imageslim)，我把在丁香医生提问的内容，原封不动地复制到春雨医生问了一遍，结果那位医生第一交互回合就只回了 2 行的短句，而且问的都是我提问里已经写清楚的内容……不排除这俩医生信息素养本来就不一样，但平台机制确实影响不小。



## 技能类课程界面

技能类课程关键在让同学乐意做作业，而方便地查看了解整期课程都有哪些作业，无疑降低了行动门槛。

### 正面案例

目前看到三节课的界面做得不错：课程主页面左边能直接查看（滑出效果）整个课程目录、右边能查看课程作业目录，不必跳转来跳转去才能看到，给用户全局感和掌控感，不易迷失。

![iasample-3jieke1.gif](http://ishanshan.zoomquiet.top/share/iasample-3jieke1.gif)

### 反面案例

相比之下，开智旧版的卡片系统就是典型的负面案例了：虽也强调输出，但用户无法快速了解整期课程作业都是什么，全是卡片，而且层级深，翻着翻着容易迷失甚至行动瘫痪：


![iasample-omc.gif](http://ishanshan.zoomquiet.top/share/iasample-omc.gif)

## CHANGELOG  

- 180819 闪闪增补卡片层级输出工具反面案例之搜索效果
- 180604 闪闪增补技能类课程界面动图
- 180403 闪闪创建

