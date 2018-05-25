# 毕业设计

# 优化天气 query 识别策略 PRD

## 项目背景

在后台随机抽取的 200 个 query ，识别为天气需求的召回率是。。准确率是。。。。仔细分析发现，可以优化天气 query 识别策略，让用户觉得百度搜索更智能。

## 项目目标

- 对天气查询需求强相关的 query ，召回率提升到。。，准确率提升到。。。
- 对天气查询需求弱相关的 query ，提供对应天气结果，实现。。的召回率，。。的准确率

## 需求概述

- 提升天气需求强相关 query 的准确率和召回率
	- 准确率：检查完善对应类目词典，保证不属于天气需求，但又包含天气相关词汇的 query 不被识别成天气需求
	- 召回率：建立出行词典，识别更多有天气需求的口语化 query 
- 调整天气需求理解规则和展示策略
	- 与天气查询强相关的 query ，保证搜索结果首条结果即可概览天气预报
	- 与天气查询弱相关的 query ，侧边栏提供简要天气预报信息，查询结果主体按现行规则展示
- 更改前端样式，优化用户体验
	- 按上条展示策略调整侧边栏样式
	- 缩短天气查询步长：与天气查询强相关的 query ，搜索结果首页即有输入框可更换查询地名

## 需求详述

### 本轮优化后，「天气查询 query」识别和展示策略介绍


#### 1. 天气查询需求可能来自哪些场景？

对抽样的 200 个 query 和日常生活经验进行分析发现，一个人若想表达了解天气预报的需求，一般都带这类词汇（以下称为 X term）：地点 where 或（和）未来时间 when 。比如明天/未来三天/下周下雨吗，北京下雨吗，北京下周下雨吗。


用户了解天气的需求一般来自以下情景：
  
- 直接表达的，该类 query 一般包含 X + Y term 。Y term 为天气查询词汇、体感词汇或天气现象词汇。比如。。。 。

	但不少歌词等综艺影视词汇或论文中也可能出现上述 term 组合，所以判断是否为天气查询需求前，需排查不含综艺影视词典和论文词典。比如。。。

- 其它希望了解天气情况的场景，主要为出行需求，比如商旅访友等，都可能要了解穿什么衣服、要不要带伞、防晒够不够等。

	那问题就比较简单了——如何判断出行？当用查询 X term +衣食住行时，就可能有出行。比如。。。

#### 2. 这些场景如何展示天气结果？

- 直接表达的，保证搜索结果首条结果即可概览天气预报，效果图详见。。。
- 了解到用户有出行需求的，则在侧边栏展示天气概况，不影响现行主体排序结果。效果图详见。。。

#### 3. 具体判断策略和所需词库

见表。。。
 
### 具体需求

#### 1. 建立和完善对应词典

需完善以下词典，见表。。。

#### 2. 调整展示策略

具体见表。。。

#### 3. 修改前端样式

需按上述示意图更新 UI 并部署到前端

#### 4. 统计需求

新策略上线后，统计被识别为 天气需求① 与 天气需求② 的 query 。


# Self Review

优点：

- 用演绎法而非归纳法思考需求识别策略，再从抽样 case 中验证策略是否可行，这样解决问题更高效
- 不仅考虑了需求识别策略，还考虑了展示策略，完整优化用户体验


改进：

待我想想……哈哈

# CHANGELOG 

- 180525 闪闪更新初稿
- 180524 闪闪创建 
