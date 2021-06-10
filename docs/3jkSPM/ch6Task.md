

# 毕业设计

> Task：经过了一段时间的训练，你终于成为了百度搜索的策略产品经理。你决定从一个优化词着手开始动手，并在后台随机抽取了200个 query （标记为1的是被机器标记为「天气」的）。请选择一部分的需求，完成一个开发量 2 周，适中版本的 PRD 设计。

目录：

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->


- [优化天气 query 识别策略 PRD](#%E4%BC%98%E5%8C%96%E5%A4%A9%E6%B0%94-query-%E8%AF%86%E5%88%AB%E7%AD%96%E7%95%A5-prd)
  - [项目背景](#%E9%A1%B9%E7%9B%AE%E8%83%8C%E6%99%AF)
  - [项目目标](#%E9%A1%B9%E7%9B%AE%E7%9B%AE%E6%A0%87)
  - [需求概述](#%E9%9C%80%E6%B1%82%E6%A6%82%E8%BF%B0)
  - [需求详述](#%E9%9C%80%E6%B1%82%E8%AF%A6%E8%BF%B0)
    - [本轮优化后，「天气查询 query」识别和展示策略介绍](#%E6%9C%AC%E8%BD%AE%E4%BC%98%E5%8C%96%E5%90%8E%E5%A4%A9%E6%B0%94%E6%9F%A5%E8%AF%A2-query%E8%AF%86%E5%88%AB%E5%92%8C%E5%B1%95%E7%A4%BA%E7%AD%96%E7%95%A5%E4%BB%8B%E7%BB%8D)
      - [1. 天气查询需求可能来自哪些场景？](#1-%E5%A4%A9%E6%B0%94%E6%9F%A5%E8%AF%A2%E9%9C%80%E6%B1%82%E5%8F%AF%E8%83%BD%E6%9D%A5%E8%87%AA%E5%93%AA%E4%BA%9B%E5%9C%BA%E6%99%AF)
      - [2. 这些场景如何展示天气结果？](#2-%E8%BF%99%E4%BA%9B%E5%9C%BA%E6%99%AF%E5%A6%82%E4%BD%95%E5%B1%95%E7%A4%BA%E5%A4%A9%E6%B0%94%E7%BB%93%E6%9E%9C)
      - [3. 具体判断策略和所需词典](#3-%E5%85%B7%E4%BD%93%E5%88%A4%E6%96%AD%E7%AD%96%E7%95%A5%E5%92%8C%E6%89%80%E9%9C%80%E8%AF%8D%E5%85%B8)
    - [需求](#%E9%9C%80%E6%B1%82)
      - [1. 建立和完善对应词典](#1-%E5%BB%BA%E7%AB%8B%E5%92%8C%E5%AE%8C%E5%96%84%E5%AF%B9%E5%BA%94%E8%AF%8D%E5%85%B8)
      - [2. 调整展示策略](#2-%E8%B0%83%E6%95%B4%E5%B1%95%E7%A4%BA%E7%AD%96%E7%95%A5)
      - [3. 修改前端样式](#3-%E4%BF%AE%E6%94%B9%E5%89%8D%E7%AB%AF%E6%A0%B7%E5%BC%8F)
      - [4. 统计需求](#4-%E7%BB%9F%E8%AE%A1%E9%9C%80%E6%B1%82)
- [自评](#%E8%87%AA%E8%AF%84)
- [CHANGELOG](#changelog)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

注：下述表格需科学上网才可访问。

# 优化天气 query 识别策略 PRD


## 项目背景

近期分析在后台[随机抽取的 200 个 query](https://docs.google.com/spreadsheets/d/1U1PrMPZmAJCmbiAAuFg0G0XoVV7xT2pxjgjSDjJwEYE/edit#gid=110956497) ，发现识别为天气需求的准确率是 77.78% ，若算上可能有天气查询需求（比如用户可能有出行需求）的 query ，召回率不到 40% 。对抽样 query 的统计分析见 [query 分类及召回率、准确率统计 - 优化百度搜索「天气查询需求识别策略」追踪表 - Google 表格](https://docs.google.com/spreadsheets/d/1U1PrMPZmAJCmbiAAuFg0G0XoVV7xT2pxjgjSDjJwEYE/edit#gid=1787312842) ：

<iframe width='750' height='820' frameborder='1' scrolling='no' src="https://docs.google.com/spreadsheets/d/e/2PACX-1vS-40rEhalEb17-koMt983rCxmJ6Uu-HenEwmhzrfDT_2IysZPCy5enl4g4kH37VdrfwD33JJjMfae_/pubhtml?gid=1787312842&amp;single=true&amp;widget=true&amp;headers=false"></iframe>

若希望用户觉得百度搜索更智能，需优化天气 query 识别策略。综合问题影响面、问题严重程度、问题解决难度和预期解决比例考虑，行动优先级见[行动优先级 - 优化百度搜索「天气查询需求识别策略」追踪表 - Google 表格](https://docs.google.com/spreadsheets/d/1U1PrMPZmAJCmbiAAuFg0G0XoVV7xT2pxjgjSDjJwEYE/edit#gid=1298137968)：

<iframe width='750' height='330' frameborder='1' scrolling='no' src="https://docs.google.com/spreadsheets/d/e/2PACX-1vS-40rEhalEb17-koMt983rCxmJ6Uu-HenEwmhzrfDT_2IysZPCy5enl4g4kH37VdrfwD33JJjMfae_/pubhtml?gid=1298137968&amp;single=true&amp;widget=true&amp;headers=false"></iframe>

若只有两周开发时间，拟先完成优先级为中、高的行动。具体需求如下：



## 项目目标

- 对天气查询需求强相关的 query ，准确率提升到至少 90%，召回率提升到至少 90% 。
- 对天气查询需求弱相关的 query ，实现 80% 的准确率， 70% 的召回率。（用户对弱需求的表达方式变数更大，所以目标设定较低）

## 需求概述

- 提升天气需求强相关 query 的准确率和召回率
	- 准确率：检查完善对应类目词典，保证不属于天气需求，但又包含天气相关词汇的 query 不被识别成天气需求
	- 召回率：建立对应词典识别出行需求，识别更多可能有天气查询需求的 query 
- 调整天气需求理解规则和展示策略
	- 与天气查询强相关的 query ，保证搜索结果首条结果即可概览天气预报
	- 与天气查询弱相关的 query ，侧边栏提供简要天气预报信息，查询结果主体按现行规则展示
- 更改前端样式，优化用户体验
	- 按上条展示策略调整侧边栏样式
	- 缩短天气查询步长：与天气查询强相关的 query ，搜索结果首页即有输入框可更换查询地名

## 需求详述

先来整体了解一下这轮调整的 big picture：

### 本轮优化后，「天气查询 query」识别和展示策略介绍


#### 1. 天气查询需求可能来自哪些场景？

对抽样的 200 个 query 和日常生活经验进行分析发现，一个人若想表达了解天气预报的需求，一般都带这类词汇（以下称为 X term）：地点 where 或（和）未来时间 when 。比如明天/未来三天/下周下雨吗，北京下雨吗，北京下周下雨吗。


用户了解天气的需求一般来自以下情景：
  
- 直接表达的，该类 query 一般包含 X + Y term 。Y term 为天气查询词汇、体感词汇或天气现象词汇。比如 `广州现在冷不冷`（no62）、`北京明天下雨吗`（no121）、`九寨沟现在温度如何`（no192）等。

	但不少歌词等综艺影视词汇或论文中也可能出现上述 term 组合，所以判断是否为天气查询需求前，需排查不含综艺影视词典和论文词典。比如 `试论我国大陆电视台天气预报节目的发展——兼谈与美国电视台天气预报节目的比较` (no110)。

- 其它希望了解天气情况的场景，主要为出行需求，比如商旅访友等，都可能要了解穿什么衣服、要不要带伞、防晒够不够等。

	那问题就比较简单了——如何判断用户有出行需求？一般来说，当用查询 X term +衣食住行时，就可能有出行。比如 `去华山需要准备什么衣服`（no63），`海口现在穿什么衣服合适`（no103），`大连自驾游`（no13），`杭州西湖四星级附近的酒店`（no116），`青海西宁五星级酒店`（no177）等。



#### 2. 这些场景如何展示天气结果？

- 直接表达的，保证搜索结果首条结果即可概览天气预报，且**可在该页直接查询天气**，demo：
	
	![coursespm-weathersearch1.png](http://ishanshan.zoomquiet.top/share/coursespm-weathersearch1.png?imageView2/2/w/1000/format/jpg|imageMogr2/size-limit/200k!)
	
	![coursespm-weathersearch.png](http://ishanshan.zoomquiet.top/share/coursespm-weathersearch.png?imageView2/2/w/1000/format/jpg|imageMogr2/size-limit/200k!)
	
- 推测用户有出行需求的，则**在侧边栏展示对应城市天气概况**，不影响现行主体排序结果。demo：

	![coursespm-weathersearch2.png](http://ishanshan.zoomquiet.top/share/coursespm-weathersearch2.png?imageView2/2/w/1000/format/jpg|imageMogr2/size-limit/200k!)


#### 3. 具体判断策略和所需词典

具体判断策略见 [词汇分类识别规则 - 优化百度搜索「天气需求识别策略」追踪表 - Google 表格](https://docs.google.com/spreadsheets/d/1U1PrMPZmAJCmbiAAuFg0G0XoVV7xT2pxjgjSDjJwEYE/edit#gid=513869170)：

<iframe width='750' height='470' frameborder='1' scrolling='no' src="https://docs.google.com/spreadsheets/d/e/2PACX-1vS-40rEhalEb17-koMt983rCxmJ6Uu-HenEwmhzrfDT_2IysZPCy5enl4g4kH37VdrfwD33JJjMfae_/pubhtml?gid=513869170&amp;single=true&amp;widget=true&amp;headers=false"></iframe>


所需词典见 [需完善的词典 - 优化百度搜索「天气查询需求识别策略」追踪表 - Google 表格](https://docs.google.com/spreadsheets/d/1U1PrMPZmAJCmbiAAuFg0G0XoVV7xT2pxjgjSDjJwEYE/edit#gid=1359304541)：

<iframe width='750' height='550' frameborder='1' scrolling='no' src="https://docs.google.com/spreadsheets/d/e/2PACX-1vS-40rEhalEb17-koMt983rCxmJ6Uu-HenEwmhzrfDT_2IysZPCy5enl4g4kH37VdrfwD33JJjMfae_/pubhtml?gid=1359304541&amp;single=true&amp;widget=true&amp;headers=false"></iframe>
 
### 需求

#### 1. 建立和完善对应词典

需完善对应词典，见上述 [需完善的词典 - 优化百度搜索「天气查询需求识别策略」追踪表 - Google 表格](https://docs.google.com/spreadsheets/d/1U1PrMPZmAJCmbiAAuFg0G0XoVV7xT2pxjgjSDjJwEYE/edit#gid=1359304541)。

#### 2. 调整展示策略

具体见上述 [词汇分类识别规则 - 优化百度搜索「天气需求识别策略」追踪表 - Google 表格](https://docs.google.com/spreadsheets/d/1U1PrMPZmAJCmbiAAuFg0G0XoVV7xT2pxjgjSDjJwEYE/edit#gid=513869170)。

#### 3. 修改前端样式

需按上述示意图更新 UI 并部署到前端。

#### 4. 统计需求

先小流量上线，统计被识别为 `天气需求 1`（含1-0与1-1）  与 `天气需求 2`（含2-0与2-1） 的 query 。效果回归，召回率和准确率达标后，再全流量上线。


# 自评

这回作业用了 10h 左右，主要花在作图、整表格、调样式什么的。想清楚词汇分类匹配规则后，感觉其它都是体力活……

优点：

- 用演绎法而非归纳法思考需求识别策略，再从抽样 case 中验证策略是否可行，这样解决问题更高效：不但可以覆盖现有 case ，还能预测未来可能出现的 case 。比如若用户输入 `凤凰古城小吃推荐` 这类「地点+吃类词汇」，也可能有出行需求，可提供天气情况。
- 用表格解决各类词汇排列组合问题，避免遗漏和混乱。
- 不仅考虑了需求识别策略，还考虑了展示策略，完整优化用户体验。


疑问：判断 query 是否属于综艺影视类目或论文类目，只能从词典排查吗？这词典维护成本得多大啊……可否从返回页面的的类型比例判断？不过查了搜索引擎工作原理，好像建页面索引时，并没有收录页面属于什么类目……



# CHANGELOG 

- 180528 闪闪在项目背景中增补 query  分析表及优先级判断
- 180526 闪闪增补图片、例子，优化格式
- 180525 闪闪更新初稿
- 180524 闪闪创建 

