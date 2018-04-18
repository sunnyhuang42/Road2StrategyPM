# Chap2 作业

> 调研豆瓣读书的书籍详情页中，「喜欢这本书的人也喜欢」这个推荐模块的效果。

## 明确需求理想态

### 该推荐模块理想状态

从公司整体业务链条来分析，该推荐模块理想状态为：

1. 用户通过该推荐模块能发现更多自己喜欢的书——进入图书详情页，并点击**想读**、**加入购书单**或**加入豆列**，最好**点击购买链接**。
2. 且如果豆瓣有该书电子版，优先引导到豆瓣电子版（豆瓣阅读）购买页。 # 创业这么多年，用户再多，能带来现金流才是王道啊。

### 用户需求分析及推荐策略猜想

用户想发现更多自己喜欢的书，通常有以下场景：

- **想主题阅读**：比如要解决某个问题，或有某些阅读偏好或习惯。这类诉求可通过同关键词推荐、同豆列推荐、同类用户（标记了想读此书，或给此书四星及以上评价）关联行为推荐、同类作者推荐、豆瓣评分等，计算出「喜欢度」指标 Top10 。
- **想系统了解某位作者的思想**，跟「人」读书：比如想读透芒格、司马贺等。这类诉求可通过作者名字直接定位其相关著作，故同作者推荐在推荐策略中权重较低即可；但若要深入了解某人思想，肯定少不了了解他人对该思想的评价，故依然需要上述主题阅读的推荐策略。

综合同关键词推荐、同豆列推荐、同类用户（标记了想读此书，或给此书四星及以上评价）关联行为推荐、同类作者推荐、豆瓣评分、同作者著作维度等，计算出「喜欢度」指标 Top10 后，又考虑到上述理想状态 2 的要求，再匹配豆瓣已有电子书目，将有电子版的图书排序适当提前。

## 抽样分析

### 样本选取

- **取样数量**：5 本（严谨取样应抽查至少 30 个样本才能代表整体情况，时间有限，所以只选了 5 个样本来示意思路）
- **取样来源**：本次调研目的是发现问题，为提升效率，特地从个人熟悉领域选了几本熟悉的，且有关联而推荐结果不太理想的 5 本图书来验证上述猜想：
	- 文献读写：
		- [会读才会写 (豆瓣)](https://book.douban.com/subject/26655043/)
		- [研究生完全求生手冊 (豆瓣)](https://book.douban.com/subject/27108502/)
	- 积极心理学：
		- [心流 (豆瓣)](https://book.douban.com/subject/27186106/)
		- [三生有幸 (豆瓣)](https://book.douban.com/subject/27663156/)
	- 育儿/脑科学：
		- [给孩子的未来脑计划 (豆瓣)](https://book.douban.com/subject/30185326/)



### 抽样情况概览






### 问题汇总及需求提炼








## 行动计划


## Self Review

这回作业花了不少时间，加起来差不多 10 小时吧，中间还不时翻翻大伙儿怎么想的……

优点：

- 不只考虑「实体书推荐模块」，而是从豆瓣整个图书推荐的角度，发觉分为「电子书」推荐和「实体书」推荐，让用户很费解，来提行动计划
- 理想态指标定得还算合理
- 能合理借助工具（zotero）减轻自己采集数据的体力活，当然如果会写脚本就省心了

改进：

- 完成作业的速度有待提高
- 如果能有时间做更多抽样，对行动优先级的判断会更有底气一些


## CHANGELOG  

- 180415 闪闪创建
