# IA003BP-Network-Science

结业项目：对网络科学形成全局认识（）

# 0、摘要


# 1、学术分析

## 1.1、时间

网络分析的由来、历史，关键节点

> 网络科学始于1934年，社会心理学家莫雷诺在1934年的著作《谁将生存？》中，借助于图论与矩阵数学，通过对青少年的研究，首次确立了今日社会网络分析的基础：社会测量及社会图。之后，1959年 Erdos 随机图理论诞生，串联概率论与图论，奠定复杂网络研究基础；1967年社会心理学家 Milgram 发现小世界现象；1973年 Granovetter 提出弱联系理论；再到1998年 Watts 发现小世界模型，开启社会网络研究与复杂网络研究的合流，导致今日网络科学的诞生。——阳志平的网志《人性与暴力——论智力侵略/讲五大元学科》

> 1999年美国圣母(Notre Dame)大学物理系的 Barabási教授及其博士生Albert在《 Science》杂志上发表了题为《随机网络中标度的涌现》一文,提出了一个无标度网络模型,发现了复杂网络的无标度性质。标志着复杂网络研究进入了网络科学的新时代,由此诞生了一门崭新的科学:网络科学。——方锦清，汪小帆等著：一门崭新的交叉科学:网络科学(上)

### 1.1.1、1936年，图论的产生。柯尼斯堡七桥。欧拉

> 该领域最早的已知论文是由Leonhard Euler在1736年撰写的着名的柯尼斯堡七桥。欧拉对顶点和边的数学描述是图论的基础，图论是研究网络结构中成对关系性质的数学分支.

![](https://upload-images.jianshu.io/upload_images/2054046-6b4ae02636cb36a5.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

上图摘自[wikipedia-Seven Bridges of Königsberg](https://en.wikipedia.org/wiki/Seven_Bridges_of_K%C3%B6nigsberg)

> 首先能想到的证明方法是把走七座桥的走法都列出来，一个一个的试验，但七座桥的所有走法共用7！=5040种，逐一试验将是很大的工作量。欧拉作为数学家，当然没那样想。欧拉把两座岛和河两岸抽象成顶点，每一座桥抽象成连接顶点的一条边.

> 考虑每进入一个点，都要从一个点出来，所以如果能返回去，每个点的边就应该是偶数条。而图中都是奇数条，所以肯定无解。

以上摘自[图论（七）哥尼斯堡七桥问题](https://blog.csdn.net/saltriver/article/details/54585595)，[百度百科-七桥问题](https://baike.baidu.com/item/%E4%B8%83%E6%A1%A5%E9%97%AE%E9%A2%98)

补充：

> 图是离散数学研究的主要对象之一。它们是天然和人造结构中最普遍存在的模型之一。他们可以在物理，生物和社会系统中模拟许多类型的关系和过程动态。在计算机科学中，它们可以代表通信网络，数据组织，计算设备，计算流程等。在数学中，它们在几何学和拓扑学的某些部分中是有用的，例如结理论。代数图论与群论有着密切的联系。
>
> 熟人和友谊图描述人们是否相互了解。影响图表模拟某些人是否可以影响他人的行为。最后，协作图模拟了两个人是否以特定方式一起工作，例如一起在电影中表演。
>
> 表达和理解现实世界系统作为网络的主题称为网络科学。

### 1.1.2、1934年，社会测量及社会图。莫雷诺。一个群体的人际结构究竟是什么样的？

原始书籍[《Who shall survive?: A new approach to the problem of human interrelations》](http://www.americandeception.com/index.php?action=downloadpdf&photo=PDFsml_AD/Who_Shall_Survive-J_L_Moreno-1978-879pgs-PSY.sml.pdf&id=290)

> 20世纪30年代美国精神病学家、社会心理学家J.L.莫雷诺提出的一种测量群体内人际吸引和排斥的方法。莫雷诺所提出的人际关系类型有 6种

![](https://upload-images.jianshu.io/upload_images/2054046-a216e36a7c81097f.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

> 这种测量法的具体步骤是向群体成员提出问题，让他们回答。例如,"请你提出你所在的团体里3个最喜欢同他们在一起工作的人，并按喜欢的程度顺次排列",“如果你们单位要派几个人出去学习，你最喜欢和谁一起去，其次喜欢和谁一起去”，等等。通过这种提问，群体内每个成员都选出了自己喜欢与之一起从事某种活动的一些人，也选出了自己不喜欢与之一起活动的一些人。对于所得结果，可以采取两种方法进行处理。一种是画出人际关系矩阵表,这是一种根据群体内总人数n而制成的n×n的行列表，表内记入各成员的选择结果，用分数表示喜欢或不喜欢的程度。例如，最喜欢为3分,其次的记2分，第三位的记1分；最不喜欢的记-3分，其次的记-2分,第三位的记-1分。这样,就可以从表上数字相加的结果一目了然地知道该群体内人际关系的情况。它既反映了群体内各个成员之间的吸引或排斥程度，也反映了该群体内谁最受欢迎，谁最不受欢迎。另一种处理结果方法是画人际关系图。图中每一小圆圈表示一个人，圆圈间的实线箭头表示一方对另一方的肯定关系，虚线箭头表示否定关系。

[百度百科-莫雷诺社会测量法](https://baike.baidu.com/item/%E8%8E%AB%E9%9B%B7%E8%AF%BA%E7%A4%BE%E4%BC%9A%E6%B5%8B%E9%87%8F%E6%B3%95)

![](https://upload-images.jianshu.io/upload_images/2054046-7437b5e9ce9c905a.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![](https://upload-images.jianshu.io/upload_images/2054046-251d449d14c26e53.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

[智库百科-莫里諾的社會測量法](https://wiki.mbalib.com/zh-tw/%E8%8E%AB%E9%87%8C%E8%AF%BA%E7%9A%84%E7%A4%BE%E4%BC%9A%E6%B5%8B%E9%87%8F%E6%B3%95)

![](https://upload-images.jianshu.io/upload_images/2054046-cbbc33af6aa19719.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
[wiki-Jacob L. Moreno](https://en.wikipedia.org/wiki/Jacob_L._Moreno)

### 1.1.3、1959,Erdős和Rényi发表的几篇论文，随机图理论诞生——Erdős–Rényi model。

原始论文1[On random graphs I](http://www.leonidzhukov.net/hse/2016/networks/papers/erdos-1959-11.pdf)

原始论文2[On the evolution of random graphs](https://pdfs.semanticscholar.org/4201/73e087bca0bdb31985e28ff69c60a129c8ef.pdf)

可以参考《网络科学引论》P250

### 1.1.4、1967年社会心理学家 Milgram 发现小世界现象

原始论文[The small world problem](http://snap.stanford.edu/class/cs224w-readings/milgram67smallworld.pdf)

> 在内布拉斯加州和波士顿任意选择的个人（N = 296）被要求与马萨诸塞州的目标人员建立熟人链，采用“小世界方法”（Milgram，1967）。64个链到达目标人。在该组中，起点和目标之间的中间人平均数为5.2。波士顿的首发链接到目标人群，其中间人数少于内布拉斯加州的中间人; 内布拉斯加州的人口群体彼此之间没有差异。注意到通过社会计量“星星”链的漏斗，48％的链条在到达目标之前通过三个人。讨论了该方法在大规模社会结构研究中的应用。

以上摘自[Stanley Milgram个人google scholar主页](https://scholar.google.com/citations?user=uw_58aEAAAAJ&hl=zh-CN)

上面的实验有漏洞，于是又有下面的实验

> 继米尔格伦的实验后，为了检验六度分隔理论的真实性，人们又进行了一些其它实验。其中一个著名的例子是“凯文·贝肯游戏”（game of Kevin Bacon）。这个游戏的主角是美国电影演员凯文·贝肯，游戏的方法是通过不停地寻找共同出演同一电影的演员，最终“找到”另一个“目标”演员。游戏里每一个演员都有一个“贝肯数”：如果一个演员与贝肯合作过电影，那么他（她）的“贝肯数”就是1。如果一个演员没有与贝肯合作过，但与某个“贝肯数”为1的演员合作过，那么他（她）的贝肯数”就是2，以此类推。比如说，吴彦祖在《80天环游世界》中与卢克·威尔逊合作过，卢克·威尔逊在《家有跳狗》中与与贝肯合作过，所以吴彦祖的“贝肯数”是2[2]。对超过133万名世界各地的演员的统计得出，他们平均的“贝肯数”是2.981[3]，最大的也仅仅是8[4]。
>
> 一个类似的结果是数学界中的“埃尔德什数”。保罗·埃尔德什就是随机图理论的开创者之一，他是著名的数学家。与他一起发表过论文的学者的“埃尔德什数”是1，与这些学者合作发表过论文的学者的“埃尔德什数”是2，以此类推。美国数学会的数据库中记录的超过40万名数学家们的“埃尔德什数”平均是4.65，最大的是13[5]。

以上摘自[维基百科-小世界网络](https://zh.wikipedia.org/wiki/%E5%B0%8F%E4%B8%96%E7%95%8C%E7%B6%B2%E8%B7%AF)

### 1.1.5、1973年 Granovetter 提出弱联系理论

原始论文[The strength of weak ties](https://sociology.stanford.edu/sites/g/files/sbiybj9501/f/publications/the_strength_of_weak_ties_and_exch_w-gans.pdf)

> 建议将社会网络分析作为将微观和宏观层面的社会学理论联系起来的工具。通过详细阐述小规模互动的一个方面的宏观含义来说明这一过程：二元关系的力量。有人认为，两个人的友谊网络的重叠程度直接取决于他们彼此联系的力量。探讨了这一原则对影响和信息传播，流动机会和社区组织的影响。强调弱关系的凝聚力。大多数网络模型隐含地处理强关系，因此将其适用性限制在小的，定义明确的群体中。强调弱关系有助于讨论两者之间的关系 群体和分析社会结构的部分，不容易根据主要群体来定义。

### 1.1.6、1998年 Watts 发现小世界模型，开启社会网络研究与复杂网络研究的合流，导致今日网络科学的诞生。

1998年，美国康奈尔大学的博士生邓肯·瓦茨（Duncan Watts）和他的导师斯蒂文·斯特罗加茨（Steven Strogatz）发表了一篇名为[Collective dynamics of 'small-world'networks(小世界网络的集体动力学)](http://leonidzhukov.net/hse/2014/socialnetworks/papers/watts-collective_dynamics-nature_1998.pdf)的论文。他们把这种现象归类为某一类复杂网络的特性。他们注意到复杂网络可以按两个独立的结构特性分类，就是集聚系数和节点间的平均路径长度。

### 1.1.7、1999年， Barabási 无标度网络

1999年美国圣母(Notre Dame)大学物理系的 Barabási教授及其博士生Albert在《 Science》杂志上发表了题为《随机网络中标度的涌现》一文,提出了一个无标度网络模型,发现了复杂网络的无标度性质。标志着复杂网络研究进入了网络科学的新时代,由此诞生了一门崭新的科学:网络科学。

## 1.2、空间

### 1.2.1、网络科学和其他学科的关系

它与数学、物理科学、复杂性科学、非线性科学、计算机与信息科学、生物科学、系统科学、 社会科学等众多学科广泛交叉。

- **网络科学涉及的相关理论方法**

![](https://upload-images.jianshu.io/upload_images/2054046-232f71a628846434.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

摘自 [方锦清，汪小帆等著：一门崭新的交叉科学:网络科学(上)](http://kns.cnki.net/KCMS/detail/detail.aspx?dbcode=CJFQ&dbname=CJFD2007&filename=WLXJ200703001&uid=WEEvREcwSlJHSldTTEYzU3EydDRPaGVMOXlJRW1QK21xZVJ2TGx2c0F4bz0=$9A4hF_YAuvQ5obgVAqNKPCYcEjKensW4IQMovwHtwkF4VYPoHbKxJw!!&v=MTE2NDRaTEc0SHRiTXJJOUZaWVI4ZVgxTHV4WVM3RGgxVDNxVHJXTTFGckNVUkxPZlp1ZHNGeURnVnJySk1pSFQ=)

- **网络科学应用的领域**

信息技术网络，计算机网络，生物圈网络，学习和认知网络，社会关系网络以及经济和金融网络。

*国际上，网络科学的顶级研究者聚集地，国家？实验室？国内，网络科学top的大学（由于网络科学是跨学科的，所以猜测每个具体学科哪个大学厉害就会涉及网络科学，比如心理学系厉害的首都师范大学的社会网络分析是top的研究机构等）*

### 1.2.2、top scientists

### 1.2.3、top journals

### 1.2.4、top labs

[Barabási Lab - Northeastern University Network Science Institute](https://www.barabasilab.com/)

[DAVID LAZER](http://www.davidlazer.com/home)



github awesome清单

学术机构、学者（github的清单里有，需要从谷歌下载前42个顶尖学者的论文）

最牛的研究者在哪里（国家、实验室、院系）

## 1.3.变量关系

### 1.3.1、范式一：定义

- **网络和网络科学的定义**

> “网络”其实就是数学中图论研究的图，由一群顶点以及它们之间所连的边构成。在网络理论中则换一套说法，用“节点”代替“顶点”，用“连结”代替“边”。复杂网络的概念，是用来描述由大量节点以及这些节点之间错综复杂的联系所构成的网络。这样的网络会出现简单网络中没有的特殊拓扑特性。

> 网络科学致力于研究复杂网络的性质，并且应用这些性质去研究一些具有网络特点的领域，比如信息技术网络，计算机网络，生物圈网络，学习和认知网络，社会关系网络以及经济和金融网络。这个领域以数学中的图论为理论基础，从物理中的统计力学，计算机科学中的数据挖掘和信息可视化，统计学中的推断建模，以及社会学和经济学中的社会结构理论等学科和分之中汲取方法论营养。

> 美国国家科研委员会（National Research Council）将网络科学定义为“研究物理，生物，和社会现象的网络化表达，创建针对这些象限具有预测效果的模型”的学科。

- **网络科学的基本概念和特征量**

![](https://upload-images.jianshu.io/upload_images/2054046-1f25b347ed2aebc3.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

摘自 [方锦清，汪小帆等著：一门崭新的交叉科学:网络科学(上)](http://kns.cnki.net/KCMS/detail/detail.aspx?dbcode=CJFQ&dbname=CJFD2007&filename=WLXJ200703001&uid=WEEvREcwSlJHSldTTEYzU3EydDRPaGVMOXlJRW1QK21xZVJ2TGx2c0F4bz0=$9A4hF_YAuvQ5obgVAqNKPCYcEjKensW4IQMovwHtwkF4VYPoHbKxJw!!&v=MTE2NDRaTEc0SHRiTXJJOUZaWVI4ZVgxTHV4WVM3RGgxVDNxVHJXTTFGckNVUkxPZlp1ZHNGeURnVnJySk1pSFQ=)

- **新模因**

结构、涌现、幂律、多层、尺度、分形、自组织、弱联系、三元组、结构洞、中心性

- **网络科学的复杂网络类型和理论模型分类**

![](https://upload-images.jianshu.io/upload_images/2054046-f39f2e7a6683dee7.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

左：按照现实的领域划分；右：根据节点度的分布特点来划分；下：根据网络的边有无权值划分；上：根据生成方式划分。

### 1.3.2、作为自变量影响什么

网络科学致力于研究节点（node）和边（edge）组成的网络（network）。节点可以从从个体、组织到国家，也可以从分子、基因到网页、地点；同样，连带可以是人际关系、组织关系与国家关系，也可以从神经网络、网页引用到交通网络。

网络科学的研究具有现实的和长远的军事国防意义；

网络科学理论可以为蓬勃发展的技术网络和网络工程等设计、防护和开发应用提供坚实的理论与技术基础；

我们一直面对社会领域复杂网络的严峻挑战,特别是,艾滋病、非典、禽流感等各种 传染病等对人类造成巨大的威胁,在特定的社会网络中传染病如何通过接触关系传播而导致流行呢？决策者如何控制这些疾病将损失降到最低限度呢？只有深入揭开复杂网络的奥秘才有希望找到这些问题的合理的答案和解决途径。

### 1.3.3、作为因变量被什么影响

 研究主题



### 1.3.4、有趣度

> 绝大多数人的思维方式是渐进的，因为有了A才有了B；A和B本是相关，但会误以为是因果。但网络科学讲究涌现、自组织。网络科学的三个高阶模型：小世界网络、随机网络、无标度网络，它们大大地拓展了人类的认知边界

> 人类开始注重结构、涌现、分形、尺度，第一次意识到原来世界不仅仅是线性因果。我们开始从亚里士多德逻辑学到多值逻辑；从频率主义到贝叶斯主义；从客观主义到体验主义；从发现物理法则到理论推演出模型。

> 网络科学作为一门交叉学科，为你提供了一个观察世界的全新视角。

# 2.商业分析

> 你不经常听到科学家说他们的领域有足够的资金。但你确实听到网络科学家的说法。麻省理工学院社会学家Damon Centola说：“现在几乎每个人都在为网络科学提供资金”，他研究了信仰和行为 - 从宗教极端主义到接种疫苗 - 如何在大型社会群体中传播。“这是进入网络科学的好时机，”他说。
>
> 美国国立卫生研究院（NIH）已在许多领域对网络方法进行了重大投资，包括癌症生物学，心血管和代谢疾病，神经生理学，人类遗传学和基因组学。该机构通过各个研究所（例如，国家普通医学研究所资助九个国家系统生物学中心，强调网络生物学的学术中心）以及通过全机构倡议（如国家网络和途径技术中心，由美国国立卫生研究院医学研究路线图和最近宣布的人类连接项目资助，旨在绘制人类大脑1000亿个神经元之间的联系。
>
> 国家科学基金会也一直在增加对网络科学的支持，特别是在致力于计算机科学和人类社会动态的部门内。Barabási说，对网络研究的军事支持也越来越多，指向由陆军，空军，海军研究办公室和国防威胁减少机构资助的研究项目。“当然，从来没有足够的钱，”他说。“但我们看到很多机构都发现这很重要，他们把钱放在嘴边。”

[Tangled Webs: Careers in Network Science](https://www.sciencemag.org/careers/2009/07/tangled-webs-careers-network-science)

# 3.职业分析


# 4.故事


# 参考资料

[wikipedia-network science](https://en.wikipedia.org/wiki/Network_science)

[awesome-network-analysis :A curated list of awesome network analysis resources. ](https://github.com/briatte/awesome-network-analysis)

[社会网络分析入门书目导读-阳志平的网志](https://www.yangzhiping.com/tech/sna-book.html)

[豆列：社会网络分析技术：探索复杂性与自组织性](https://www.douban.com/doulist/1380669/?start=25&sort=time&playable=0&sub_type=)

[小世界现象，从W-S模型到W-S-K模型](https://zhuanlan.zhihu.com/p/30726433)


# changelog

- 190107 搜索自己感兴趣的主题对应的学习，了解神经科学、认知科学、心理科学等。

- 190108 搜索五大元学科，选择对网络科学形成全局认识作为结业项目

- 190109 写下初步的思路框架

- 190113 初步扩充好学术分析的时空变量内容

-
