# 先做大功能模块，还是优化型需求？

产品开发到底应该先做大的功能模块，还是优化原有功能？

之前想当然地认为是前者：先把咱们设想中的产品架子搭起来，再优化那些不影响使用的细节，毕竟互联网产品嘛，谁慢谁出局。但现在觉得并非如此，得看具体情况。

比如音频倍速播放，这属于优化型需求，没有用户也可以听音频。但对于一款早期的内容型 App ，这个真的只是优化型需求吗？未必，尤其在现在用户越来越习惯倍速收听的形势下，没有倍速播放简直可以拖出去斩了 —— 人一旦习惯了高倍速的声音信息输入，便很难再回去，要不觉得浪费时间（同样的时间我为什么不听单位时间信息量更大的？），要不昏昏欲睡或不断走神。

我就经常陷于这样的困扰：深知我司生产的育儿内容很好，身为团队成员我应该且也有兴趣多了解这些内容，也乐意为自家 App 的 DAU 做些贡献；何况自己每天做不需要脑的事情（比如梳洗、家务）时都会听些音频。但坦白说，自家 App 音频不能倍速播放，这一个细节就把它挡在我每天启动的 App 之外，导致它每周被我主动启动的次数不超过 3 次……推己及人，目测也有部分家长和我状况类似。这款 App 正处于上线早期，这是培养用户使用习惯的阶段，如果一开始用户就没觉得有频繁使用的动力，那这 App 在他们心中的重要性就不可避免地降低，之后再激活他们关注便困难不少。那时即使咱们有再多新的功能模块，他们可能都没注意到……细思恐极，但愿和我情况类似的家长较少吧。

App 使用数据采集和分析也类似。团队开发资源紧张，所以数据需求总被排在功能需求之后。乍一看挺合理的：对外的事情最重要嘛，数据采集和分析，用户又不能直接感受到，上得慢点或不用心也没关系。

真的如此吗？不。互联网创业项目拼速度，私以为更应该一开始就在数据采集和分析上下功夫——此时是验证原型阶段，快速验证各类假设、调整猜想最重要，尤其很多时候各类决策是团队拍脑袋想出来的，更需快速验证、调整。如何验证？市场反馈、用户数据啊。不是傻不愣登地问用户这个产品或模块你觉得如何，你为什么不用，你有什么优化建议，而是看各类数据，比如他们是什么时间访问的，每次访问路径是怎样的，各页面停留多久，什么东西根本没碰；然后基于这些数据提出几种假设，快速调整、继续观察，并配合一些深度访谈获取更多用户数据，继续猜想、调整、验证。

如此，若数据功能跟不上，有何后果？幸运点的话，即使团队没有那么多用户数据，也眼光犀利如乔帮主，洞察用户心思，拿出令用户爱不释手的产品；不走运的话，那就可能在干低水平的体力活这条路走到黑咯……


## CHANGELOG  

- 180318 闪闪创建
