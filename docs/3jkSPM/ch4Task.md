
# Chap4 作业



> Task：完成一份「微博搜索」竞品分析报告。参考课程中【实例】网页搜索策略思考方法，验证微博中的具体状况，针对这些用户需求以及不足的点，提出优化方案。

目录：

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->


- [「微博搜索」竞品分析报告](#%E5%BE%AE%E5%8D%9A%E6%90%9C%E7%B4%A2%E7%AB%9E%E5%93%81%E5%88%86%E6%9E%90%E6%8A%A5%E5%91%8A)
  - [分析目的与执行概要](#%E5%88%86%E6%9E%90%E7%9B%AE%E7%9A%84%E4%B8%8E%E6%89%A7%E8%A1%8C%E6%A6%82%E8%A6%81)
    - [分析目的](#%E5%88%86%E6%9E%90%E7%9B%AE%E7%9A%84)
    - [分析对象](#%E5%88%86%E6%9E%90%E5%AF%B9%E8%B1%A1)
    - [分析方法](#%E5%88%86%E6%9E%90%E6%96%B9%E6%B3%95)
  - [分析结果综述](#%E5%88%86%E6%9E%90%E7%BB%93%E6%9E%9C%E7%BB%BC%E8%BF%B0)
  - [分析详述](#%E5%88%86%E6%9E%90%E8%AF%A6%E8%BF%B0)
    - [明确产品定位和分析方向](#%E6%98%8E%E7%A1%AE%E4%BA%A7%E5%93%81%E5%AE%9A%E4%BD%8D%E5%92%8C%E5%88%86%E6%9E%90%E6%96%B9%E5%90%91)
    - [对比竞品](#%E5%AF%B9%E6%AF%94%E7%AB%9E%E5%93%81)
      - [维度一：微博搜索在「需求理解、排序策略、展现策略」上值得做的调整](#%E7%BB%B4%E5%BA%A6%E4%B8%80%E5%BE%AE%E5%8D%9A%E6%90%9C%E7%B4%A2%E5%9C%A8%E9%9C%80%E6%B1%82%E7%90%86%E8%A7%A3%E6%8E%92%E5%BA%8F%E7%AD%96%E7%95%A5%E5%B1%95%E7%8E%B0%E7%AD%96%E7%95%A5%E4%B8%8A%E5%80%BC%E5%BE%97%E5%81%9A%E7%9A%84%E8%B0%83%E6%95%B4)
      - [维度二：微博搜索在「影视综艺」主题上值得做的调整](#%E7%BB%B4%E5%BA%A6%E4%BA%8C%E5%BE%AE%E5%8D%9A%E6%90%9C%E7%B4%A2%E5%9C%A8%E5%BD%B1%E8%A7%86%E7%BB%BC%E8%89%BA%E4%B8%BB%E9%A2%98%E4%B8%8A%E5%80%BC%E5%BE%97%E5%81%9A%E7%9A%84%E8%B0%83%E6%95%B4)
      - [维度三：微博搜索在「高效了解某位用户的情况」方向上值得做的调整](#%E7%BB%B4%E5%BA%A6%E4%B8%89%E5%BE%AE%E5%8D%9A%E6%90%9C%E7%B4%A2%E5%9C%A8%E9%AB%98%E6%95%88%E4%BA%86%E8%A7%A3%E6%9F%90%E4%BD%8D%E7%94%A8%E6%88%B7%E7%9A%84%E6%83%85%E5%86%B5%E6%96%B9%E5%90%91%E4%B8%8A%E5%80%BC%E5%BE%97%E5%81%9A%E7%9A%84%E8%B0%83%E6%95%B4)
    - [梳理需求优先级](#%E6%A2%B3%E7%90%86%E9%9C%80%E6%B1%82%E4%BC%98%E5%85%88%E7%BA%A7)
- [自评](#%E8%87%AA%E8%AF%84)
- [CHANGELOG](#changelog)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

注意：下述表格需在科学上网模式下才可访问。

# 「微博搜索」竞品分析报告


## 分析目的与执行概要

### 分析目的

通过了解同类产品做法和效果，梳理「微博搜索」模块若想更好地实现其应承担的效用，可做哪些调整。

### 分析对象

本次分析对象主要有三类：

1. 微博同类产品的搜索功能比对。分析对象为微博 App ，国内泛社交应用微信，国外和微博部分类似的 App Facebook、Twitter、Instagram 。
2. 泛娱乐场景下，解决观影需求的产品搜索功能比对。分析对象为微博，豆瓣（腾讯系、国内在该维度上领先的产品）、IMDb（国外用户发布影评、艺人作品展示的主要平台）。
3. 高效了解某位用户情况的诉求下，微博值得做哪些调整。分析对象为微博、国外这块做得较好的 Facebook 。

### 分析方法

时间精力有限，本次分析主要从官方资料、网友评论、个人手动测试验证获取数据，以找出「微博搜索」在需求理解、排序策略、展现策略等方面值得做的调整。

## 分析结果综述

现有的需求理解策略基本能满足大众用户需求，不尽快优化尚无大碍。

如果想让这个模块对整个产品产生更大的价值，建议做这些调整，见 [ProjectPriority - 微博搜索竞品分析追踪表 - Google 表格](https://docs.google.com/spreadsheets/d/1C59UgiXD8LW5CS9wNG3kB17_UvTVgJeKZF0ZudDigaQ/edit#gid=1691955735) ：

<iframe width='750' height='290' frameborder='1' scrolling='no' src="https://docs.google.com/spreadsheets/d/e/2PACX-1vR_kco1oSm4nZLayKebJrDQ4wJ6gdPRly8tzg_OiNT1Km6y9ok2Vq4l39PB2ow8njYf0UY7Ewi2a-qr/pubhtml?gid=1691955735&amp;single=true&amp;widget=true&amp;headers=false"></iframe>

## 分析详述

### 明确产品定位和分析方向

从微博[财报](http://ir.weibo.com/phoenix.zhtml?c=253076&p=irol-newsArticle&ID=2332019)（看不懂可以多翻业界对其财报的解读，比如[这个](https://mp.weixin.qq.com/s/RHVEYaFenQ6ad0tynMzXGA)）、[App store 产品介绍](https://itunes.apple.com/cn/app/%E5%BE%AE%E5%8D%9A/id350962117?mt=8)、[微博搜索官方文档](https://help.weibo.com/newtopic/search/list/1968)和[用户报告](http://data.weibo.com/report/reportDetail?id=404)、公司高管发言等材料发现，微博主要有以下特征：

- 是国内用户尤其红人发布或了解全网实时观点的第一平台
- 主要收入来源为广告营销（近九成）
- 用户特征
	- 用户在三线及三线以下城市占比过半（52.6%），且未来 1-2 年依然走「下沉到三四五六七八线城市」路线
	- 用户主要活跃在移动端（92%）
	- 用户关注领域主要为吃喝玩乐，尤其影视综艺、美妆
- 短视频、直播是现阶段流量洼地，也是微博不想错过的红利



由此推测：

- 微博若想在国内腾讯系、头条系社交产品和短视频产品的夹击下，继续保持甚至提升 DAU & MAU 增速，成为用户杀时间舍不掉的选择，需要**能给用户提供别家无法提供的价值**。而实时了解红人状态、和红人互动，是微博相较国内其它产品最大的特色和优势。
- 「微博搜索」模块可利用用户行为数据放大这一优势，促进  DAU & MAU 提升。比如基于搜索日志推荐更可能查看、付费的内容和广告，基于公开的用户数据提供一些特殊功能以便用户高效了解某位用户的情况或全网对某个事件的态度等。

综上，拟分析如下方向：

- 主要分析微博**移动端**而非网页版的搜索效果，因为九成以上的访问来自移动端，移动端的体验更值得团队下功夫。
- 挖掘「微博搜索」在影视综艺主题上值得做的调整。
- 关注微博在「高效了解某位用户的情况」方向的现有效果及同类产品值得借鉴之处。


### 对比竞品

#### 维度一：微博搜索在「需求理解、排序策略、展现策略」上值得做的调整

在该维度上，主要以微信、Facebook、Twitter、Instagram 和微博比对。

![coursespm-weibosearch.003.jpeg](http://ishanshan.zoomquiet.top/share/coursespm-weibosearch.003.jpeg?imageMogr2/size-limit/100k!)

截至 2018-05-22 17:00 ，上述五个 App 最新版本的情况见 [CompetitiveAnalysisV1 - 微博搜索竞品分析追踪表 - Google 表格](https://docs.google.com/spreadsheets/d/1C59UgiXD8LW5CS9wNG3kB17_UvTVgJeKZF0ZudDigaQ/edit#gid=1835244465)：

<iframe width='750' height='800' frameborder='1' scrolling='no' src="https://docs.google.com/spreadsheets/d/e/2PACX-1vR_kco1oSm4nZLayKebJrDQ4wJ6gdPRly8tzg_OiNT1Km6y9ok2Vq4l39PB2ow8njYf0UY7Ewi2a-qr/pubhtml?gid=1835244465&amp;single=true&amp;widget=true&amp;headers=false"></iframe>

由表中记录和测试观察，发现微博搜索在该维度上

可圈可点的细节：



- 现行的需求理解策略已基本能满足大多数用户的需求。原因如下：
  - **泛娱乐类**的**大众**搜索诉求一般比较简单，且微博给用户的心智定位就是了解最新动态，所以用户检索多以事件名称或人名为主。[微博热搜榜](http://s.weibo.com/top/summary?cate=realtimehot)也侧面印证了这点——用户搜索的 query 多数结构简单，较少涉及口语化搜索或复杂表达。
  - 而那些有精准搜索需求的高阶用户，也不会只依靠微博搜索。
  - 在同类产品如 微信、Facebook、Twitter、Instagram 中，微博的需求理解策略尚无量级差异。且很难因为微博的搜索结果更令人满意， DAU & MAU 就有较大提高。
  - 所以，即使现行需求理解策略离 [Google 这样 search engine 标杆](https://www.hackcollege.com/blog/2011/11/23/infographic-get-more-out-of-google.html) 相差甚远，也已够用。如有更优先的需求，现行需求理解策略暂不优化也无大碍。
- 搜索入口与推荐内容主页共用「discover」入口，既令底部菜单栏导航清晰降低认知负荷，又助用户杀时间。
  - 玩微博的用户，多数希望找乐子消遣。这个入口既可检索自己感兴趣的主题，又提供有很多内容。即使用户需求不明确，也能在这里随便看看杀时间。
  - 且该页面下拉后进入的页面 `video/story/news/list/Your city` 导航设计也合理，video 符合短视频趋势，story 是微博当前主推的新功能。
- 检索关键词后出现会出现置顶的 filters 导航 `综合/用户/实时/关注/视频/文章/图片/热门/印象/话题/主页/更多` ，很好，尤其这俩 filters:
	- 「关注」：可只查看我关注（follow）的人对这件事的看法，隔离闲杂人等
	- 「印象」：可方便了解全网对当前关键词的关注点有哪些，了解舆情
		![coursespm-weibosearch.001.jpeg](http://ishanshan.zoomquiet.top/share/coursespm-weibosearch.001.jpeg?imageMogr2/size-limit/100k!) 
	
	- 这两标签技术含量对不高，但属其它平台没有的特性，是微博的独特价值。若想放大，可在「印象」中增加对「关注」内容里的词云呈现，便于用户快速了解所关注用户对某个关键词的的态度。如此更能吸引一波有研究诉求的用户。


值得做的调整如下：

- 检索结果飘红关键词。鉴于搜索结果中常有 @ 、链接等变色字段，建议选择**同色加粗**的飘红方式。
- 插入广告的姿势更温柔，停止强势插入，保护用户体验。

	测试时发现若有广告主买了对应关键词，则搜索时广告会霸占首屏。比如我检索「复仇者联盟」时结果如左下图：
	
	![coursespm-weibosearch.002.jpeg](http://ishanshan.zoomquiet.top/share/coursespm-weibosearch.002.jpeg?imageMogr2/size-limit/100k!)
	
	看到这个我第一反应是「难度输错关键词了？」确认输入无误，且三天内检索了同一关键词四五次，我从没点击它还依然在，对微博和这个广告主印象分下降不少。推测其他用户也有类似体验。那这对微博和广告主来说都亏：于微博，没捞到钱，还损失了口碑；于广告主，花钱打市场，实际付费转化没多少，还掉了口碑。

  所以，建议更温和和智能一些。比如碰到这个广告出 3 次都没点击，广告就撤销，或者换个广告。以及呈现综艺类内容检索结果时，有广告也给出电影主页入口，类似上图。


#### 维度二：微博搜索在「影视综艺」主题上值得做的调整


在该维度上，主要以豆瓣、IMDb 和微博比对。

![coursespm-weibosearch.004.jpeg](http://ishanshan.zoomquiet.top/share/coursespm-weibosearch.004.jpeg?imageMogr2/size-limit/100k!)

截至 2018-05-22 17:00 ，上述三个 App 最新版本的情况见 [CompetitiveAnalysisV2 - 微博搜索竞品分析追踪表 - Google 表格](https://docs.google.com/spreadsheets/d/1C59UgiXD8LW5CS9wNG3kB17_UvTVgJeKZF0ZudDigaQ/edit#gid=1709836654)：

<iframe width='750' height='800' frameborder='1' scrolling='no' src="https://docs.google.com/spreadsheets/d/e/2PACX-1vR_kco1oSm4nZLayKebJrDQ4wJ6gdPRly8tzg_OiNT1Km6y9ok2Vq4l39PB2ow8njYf0UY7Ewi2a-qr/pubhtml?gid=1709836654&amp;single=true&amp;widget=true&amp;headers=false"></iframe>

由表中记录和测试过程，发现微博搜索在该维度上最大的优势，是可直接查看相关人员的微博，了解其最新动态。

用户搜索影视综艺内容，最期待找得到、看得着。目前微博已内置购票入口，在映电影可直接购票。但过往作品没法直接查看。建议增加影视资源观看入口。可接入同属阿里系下的影视资源平台爱奇艺、优酷的播放入口，既提升用户体验，还可收买路钱增加营收。

操作可类似豆瓣：

![coursespm-weibosearch-douban3.png](http://ishanshan.zoomquiet.top/share/coursespm-weibosearch-douban3.png?imageView2/2/w/1000/format/jpg|imageMogr2/size-limit/100k!)



#### 维度三：微博搜索在「高效了解某位用户的情况」方向上值得做的调整


在该维度上，主要以 Facebook 和微博比对。

Facebook 在 2013 年初推出了[ graph search 功能](https://en.wikipedia.org/wiki/Facebook_Graph_Search)，能理解自然语言，且基于你的关系网给你答案。微博随后也推出了[图谱搜索功能](https://help.weibo.com/newtopic/search/list/1960?sudaref=help.weibo.com)：

> 通过图谱搜索，您可以找到去过某个景点、读过某本书、听过某首音乐、评论过某部电影、赞过某个餐馆等的好友，让您在好友中找到与您最投缘的人。


但这两天测试发现，除了支持与、或、非 3 种常见语法搜索外，其它更高阶的搜索功能基本都已失效。暂未检索到此功能下线原因，介于其[上线时亦低调](http://gejia021.blog.techweb.com.cn/archives/313.html)，推测是图谱功能若要进一步迭代成本太高，而国内亦有大众点评、豆瓣等主流平台满足上述提及的图谱需求，留着也鸡肋，所以低调下线。

结合前述分析，国内最大的竞争对手微信，已引入更多内容来源，令用户可以解决很多在微博上也能解决的搜索需求。而微博最大的特色是，这里属红人的社交账号，发声的第一平台。

由此，微博搜索若想让用户难以离开，值得强化对「人」的搜索：不必像 Facebook graph search 那么复杂，毕竟国内吃喝玩乐推荐有已占领用户心智的「大众点评」。可优先恢复这些之前做过的、使用公开数据的功能：

- 了解某位用户的兴趣爱好：方便的搜索到某个指定用户（如喜欢的某个明星）赞过的所有事物。详见[搜索帮助](https://help.weibo.com/newtopic/search/list/1960?sudaref=help.weibo.com)中 `如何发现某用户（某明星）的兴趣爱好？`。 
- 了解某几位用户的共同好友：输入你查询的用户微博昵称，就可以知道他们之间有没有共同好友啦：

	![coursespm-weibosearch1.png](http://ishanshan.zoomquiet.top/share/coursespm-weibosearch1.png)

此后若有研发能力，再做更多拓展，比如了解某位用户的关注点——对指定用户微博内容做词云分析等。

### 梳理需求优先级

优先级判断主要考虑以下角度：问题严重/重要程度、问题影响面、解决成本、预期解决比例，由于预期解决比例难以评估，故分析中略去。综合梳理得出微博搜索模块值得做的调整和优先级，详见[ProjectPriorityV0 - 微博搜索竞品分析追踪表 - Google 表格](https://docs.google.com/spreadsheets/d/1C59UgiXD8LW5CS9wNG3kB17_UvTVgJeKZF0ZudDigaQ/edit#gid=470309809) ：

<iframe width='750' height='290' frameborder='1' scrolling='no' src="https://docs.google.com/spreadsheets/d/e/2PACX-1vR_kco1oSm4nZLayKebJrDQ4wJ6gdPRly8tzg_OiNT1Km6y9ok2Vq4l39PB2ow8njYf0UY7Ewi2a-qr/pubhtml?gid=470309809&amp;single=true&amp;widget=true&amp;headers=false"></iframe>

# 自评


本次作业，花了 40 多小时吧……大半花在前期找查资料、梳理微博搜索应实现什么效用，以及测试对比各产品。尤其这几个产品多是杀时间利器，测着测着一不小心就开始看起视频来（捂脸）……不管怎样，总算搞定。

优点：

- 一如既往地自顶向下考量，拿到任务下意识地先思考这个产品要解决什么问题，可以给用户什么独特价值，这个模块要实现怎样的效用、在整个业务体系中扮演什么角色。
- 遇到问题习惯性地先查官方文档，比如「微博搜索」及竞品的官方文档，微博用户的官方数据，通过一手信息了解官方意图。
- 选了三个分析维度，且选取合理。


改进：

- 对具体排序策略可以测得细致。但情况太多穷举不尽，且时间有限就先这样吧。实际工作中可以找 RD 一起测试分析，他经验丰富更能精准摸出具体算法规则。
- 对于新功能新场景的畅想可以更开阔，这才是创造产品的乐趣源泉嘛。

PS.

调研过程翻到不少有意思的评论、新闻，有助思考微博及微博搜索模块当如何调整。现把上文未列出的附在这里，以备日后取用，也供感兴趣的朋友了解：

* Hallanan, L. (2017, October 19). Weibo is NOT China’s Twitter! Retrieved  from http://www.parklu.com/weibo-not-chinas-twitter/
* Twitter工程师眼中的新浪微博-搜狐IT. (n.d.). Retrieved  from http://it.sohu.com/20130510/n375396327.shtml
* 叶施仁, 严水歌, & 杨长春. (2013). 新浪微博搜索排序方法研究. 常州大学学报(自然科学版), (03), 71–75. Retrieved from http://oversea.cnki.net/kcms/detail/detailall.aspx?filename=jssy201303019&dbcode=CJFQ&dbname=CJFQTOTAL
- Graph Search
	* Facebook Announces Its Third Pillar “Graph Search” That Gives You Answers, Not Links Like Google. (2013, January 15). Retrieved  from http://social.techcrunch.com/2013/01/15/facebook-announces-its-third-pillar-graph-search/
	* Walker, L. (n.d.-a). Facebook Search: A Complete Beginner’s Guide. Retrieved  from https://www.lifewire.com/facebook-search-guide-to-searching-facebook-2654608
	* Walker, L. (n.d.-b). Find Out How Graph Search on Facebook Works for You. Retrieved  from https://www.lifewire.com/facebook-advanced-search-tips-2653972
	* FacebookGraphSearch - GetIt01. (n.d.). Retrieved  from https://www.getit01.com/tag/FacebookGraphSearch/
	* Facebook 能搜索。新浪微博能搜索么？. (2013, January 16). Retrieved  from http://www.ifanr.com/235818
- 新浪用户行为报告
	* 2016微博用户发展报告.pdf. (n.d.). Retrieved from http://data.weibo.com/report/file/view?download_name=3b895b5c-6010-f5fb-8001-a1e9d14d7bc4&file-type=.pdf
	* 2017科技用户分析报告.pdf. (n.d.). Retrieved from http://data.weibo.com/report/file/view?download_name=3aa1aa9d-2b77-1034-9a3c-7c809d005963&file-type=.pdf
	* 微博化妆品报告.pdf. (n.d.). Retrieved from http://data.weibo.com/report/file/view?download_name=153a3e47-c4b7-dcc5-2690-f2ee73162d41&file-type=.pdf


# CHANGELOG 

- 180524 闪闪增补 PS
- 180523 闪闪完善正文、增补数据和配图
- 180522 闪闪更新分析框架
- 180520 闪闪创建

