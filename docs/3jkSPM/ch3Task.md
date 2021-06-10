
# Chap3 作业


本次作业包括以下板块：

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->


- [Part1：小红书优化购买流程需求文档](#part1%E5%B0%8F%E7%BA%A2%E4%B9%A6%E4%BC%98%E5%8C%96%E8%B4%AD%E4%B9%B0%E6%B5%81%E7%A8%8B%E9%9C%80%E6%B1%82%E6%96%87%E6%A1%A3)
  - [项目背景](#%E9%A1%B9%E7%9B%AE%E8%83%8C%E6%99%AF)
  - [项目目标](#%E9%A1%B9%E7%9B%AE%E7%9B%AE%E6%A0%87)
  - [竞品调研](#%E7%AB%9E%E5%93%81%E8%B0%83%E7%A0%94)
  - [需求概述](#%E9%9C%80%E6%B1%82%E6%A6%82%E8%BF%B0)
  - [需求详述](#%E9%9C%80%E6%B1%82%E8%AF%A6%E8%BF%B0)
    - [1. 增加一键再次下单功能](#1-%E5%A2%9E%E5%8A%A0%E4%B8%80%E9%94%AE%E5%86%8D%E6%AC%A1%E4%B8%8B%E5%8D%95%E5%8A%9F%E8%83%BD)
    - [2. 增加订单即将超时提醒机制](#2-%E5%A2%9E%E5%8A%A0%E8%AE%A2%E5%8D%95%E5%8D%B3%E5%B0%86%E8%B6%85%E6%97%B6%E6%8F%90%E9%86%92%E6%9C%BA%E5%88%B6)
    - [3. 差异化订单支付时限](#3-%E5%B7%AE%E5%BC%82%E5%8C%96%E8%AE%A2%E5%8D%95%E6%94%AF%E4%BB%98%E6%97%B6%E9%99%90)
    - [4. 统计需求](#4-%E7%BB%9F%E8%AE%A1%E9%9C%80%E6%B1%82)
- [Part2：课后思考题](#part2%E8%AF%BE%E5%90%8E%E6%80%9D%E8%80%83%E9%A2%98)
- [自评](#%E8%87%AA%E8%AF%84)
- [CHANGELOG](#changelog)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

注意：以下表格需在科学上网模式下才可访问。

---

Part1 Task：

> 小红书现在的产品逻辑是不管什么样的用户，都会以 30mins 内没付款，就取消交易。分析发现 3% 的用户会在订单取消后，30mins~120mins 内二次生成生成订单，二次购买。

> 你作为策略产品经理，认为现在的这种时间限制对应有点阻碍用户体验，有必要用策略的手段优化这一问题。请为此撰写一份 PRD ，给出一个针对不同场景不同用户下，不同的时长方案。

# Part1：小红书优化购买流程需求文档



## 项目背景

小红书现在的产品逻辑是不管什么样的用户、什么样的商品，都会以 30mins 内没付款，就取消交易。分析发现 3% 的用户会在订单取消后，30mins~120mins 内二次生成生成订单，二次购买。

仔细分析现有购买流程和竞品做法，发现可做一些优化，提升用户体验和订单总成交率。

## 项目目标

通过优化购买流程，提升订单总成交率：使当前成交率 n ，同比增长 5-10% （实际工作中此同比增长目标需根据公司过往订单成交率、订单取消率、订单自动取消率、业内中位数调整） 。


## 竞品调研

同类产品购买流程调研结果见 [同类平台购物体验-小红书购物流程优化追踪表 - Google 表格](https://docs.google.com/spreadsheets/d/1sz5MgZurOmPb4928bjzvG2M4DrXmkem9ngeN-36kXmY/edit#gid=0)：

<iframe iframe width='750' height='860' frameborder='1' scrolling='no' src="https://docs.google.com/spreadsheets/d/e/2PACX-1vQzCWGh28gtnVGbt5X63ysl0P3gJYPs-Wb5_9t35MFUpeLIsgpdwinhHROSlSuoyvWg9wb_gup2rFHy/pubhtml?gid=224436884&amp;single=true&amp;widget=true&amp;headers=false"></iframe>


## 需求概述

优化目前购买流程里几处体验，以提升订单成交率。主要优化以下不足：

1. 已有订单（包括待付款、待收货、已完成、已取消状态）无法一键再次下单，用户必须逐个点击商品详情加入购物车
2. 订单超时未支付自动取消前，用户没收到任何提醒
3. 订单自动取消时长不灵活，千人一面：
	* 什么样的商品都是一样的订单自动取消时间
		* 促销
			* 库存紧张（<=5）
			* 库存不紧张（>5）
		* 常规
			* 库存紧张（<=5）
			* 库存不紧张（>5）
	* 什么样的用户都是一样的订单自动取消时间
		* 黑卡
		* 非黑卡


## 需求详述

注：若成本有限（工期/资金），以下需求优先级为 1>2>3

### 1. 增加一键再次下单功能

在已有订单（包括待付款、待收货、已完成、已取消状态）中增加「再次购买」入口，以便用户快速再次下单。具体页面逻辑如下 ：


![pmcoursech3xhs-1.png](http://ishanshan.zoomquiet.top/share/pmcoursech3xhs-1.png)
（原图地址：https://www.processon.com/view/link/5afbd825e4b00268626785ec ）

### 2. 增加订单即将超时提醒机制

在现有超时自动取消的订单中，97% 的用户没在 120 mins 内回来再次下单，分析原因见 [未二次下单原因分析 - 小红书购买流程优化追踪表 - Google 表格](https://docs.google.com/spreadsheets/d/1sz5MgZurOmPb4928bjzvG2M4DrXmkem9ngeN-36kXmY/edit#gid=0)：

<iframe iframe width='500' height='300' frameborder='1' scrolling='no' src="https://docs.google.com/spreadsheets/d/e/2PACX-1vQzCWGh28gtnVGbt5X63ysl0P3gJYPs-Wb5_9t35MFUpeLIsgpdwinhHROSlSuoyvWg9wb_gup2rFHy/pubhtml?gid=0&amp;single=true&amp;widget=true&amp;headers=false"></iframe>

由于上述情况后台难以区分，且高挽回难度的情况难以提供效解决方案，故统一按挽回难度低的情况处理。

综上，结合小红书用户使用习惯和成本，拟增加以下提醒机制：

- 支付时限剩 1/2 时，自动给用户发送 App push 消息+ 短信提醒，提醒文案如下：

	>你看上的<商品名称>等商品，< N >位小红薯也想要！卖家存货不多，还有< X/2 >分钟订单将自动取消，你再不来支付别人就抢走啦 < orderlink > >_<

	`< >` 内容根据订单情况自动替换：
	
	- <商品名称> 为订单中月销量最大的商品名称
	- < N > 为订单所有商品在小红书平台呢加入购物车件数总量
	- < X/2 > 为订单支付时限的 1/2 ，四舍五入保留整数
	- < orderlink > 为订单页面链接
		- 若为 App push 消息，不显示该字段，点击消息框即直接跳转 App 订单页面
		- 若为短信消息，用户点击该链接可自动跳转 App 订单页面（可参考唯品会的做法：点击链接跳转手机默认浏览器进入 App 下载页，页面提示 `open this page on 「聚美优品」？`，点击确认即跳转 App 订单页面）
- 若成本有限（工期/资金），优先保证 App push 消息

### 3. 差异化订单支付时限

出于释放库存的考虑，下了订单后，这个库存被暂时锁定，方便库存计算，防止大量并发库存不够用，同时也防止长期占用库存，导致库存计算困难，这个需求是时间越短越好。

但结合上述竞品调研结果和小红书已形成的用户认知，拟继续保持 30mins 支付时限。不过对不同商品和不同用户按如下规则做微调，见下述支付时限判断规则：

![pmcoursech3xhs-4.png](http://ishanshan.zoomquiet.top/share/pmcoursech3xhs-4.png)
（原图地址：https://www.processon.com/view/link/59706f1ee4b01fc0fe2031bc ） 

浮框提示文案：

- 1：

	> 您刚才选择的商品没有支付成，已生成订单，请在 30 分钟内完成支付，避免宝贝贝抢完啦。

	>（选项） 去付款 再等等

- 2：

	> 订单中有抢手商品，X 分钟内未支付，订单将自动取消。别让心仪的 ta 被别人抢走啦！

	>（选项） 去付款 再等等


### 4. 统计需求

为评估本轮优化效果，需统计上线后的：

- 一次成单率
- 订单自动取消率
- 订单自动取消后的二次购买率、二次购买时长间隔

# Part2：课后思考题

- Q1:

	> 如果用户行为判断不出男女，但可以从其自己填的信息（比如性别或身份证）判断为女，那在定义标签时是否应该定为女？
  
	不应该，直接标定 男+女 的标签即可。不管其真实性别如何，其行为特征表明其对男性和女性用户感兴趣的信息都可能有兴趣。

- Q2:

	> 为什么滴滴的默认推荐「回家」可以直接点击，美团外卖和微博的默认推荐，只放在搜索框里？
  
	因为用户场景不同，后者候选范围太广，且用户偏好多变，猜中准确率太低，没必要设为一步到位的效果。

- Q3:

	> 为什么微博是需要输入完整的词，而非类似美团外卖京东到京等，直接在输入拼音的时候就猜
  
	因为前者候选数据量太大，加载慢，若在输入拼音的时候就猜，牺牲的体验不如得到的体验，故舍弃。

# 自评

本次作业前后花了差不多 20h ，有了这回的经验教训，相信下回可以更快。

优点：

- 从业务全局思考，直接定出的目标是提升整体订单成交率，而非某个现象导出的局部目标
- 有多个需求时，给出了需求优先级，以便工程组提升 ROI


改进：在作业上没想到什么必须改的了……哈哈。不过作业的过程倒是挺多教训的，更多思考见 https://road2strategypm.ishanshan.im/Course3jkSPM/Chap3Review.html 。

# CHANGELOG 

- 180603 闪闪删除项目目标中「提升用户体验」的描述
- 180517 闪闪修正细节
- 180516 闪闪更新初稿
- 180514 闪闪创建

