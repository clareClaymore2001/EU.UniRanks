# 欢迎来到克莱尔欧洲大学排名（Clare EU UniRanks）！

在各种润学论坛，可以说三分之一的问题都是选校选offer，尤其是欧陆，简直是重灾区。当然，这是由于欧陆院校普遍曝光度小、知名度差的原因，导致去除超一流院校后很难区分院校层次。这种时候，可见排名的重要性。然而，常见的排名比如 QS 之类的问题懂得都懂、不再赘述，而即使是 Nature Index 或者 CS Rankings 之流，也很难给出一个令人满意的答案。

这里介绍一种个人认为极其科学的大学排名方法，用以量化院校的可读性。可以说，虽然做不到完美拟合院校真实实力，但也是无限逼近，起码参考性上也是秒杀当今所有知名排名。

当然，我个人是没有那么多精力统计完所有的院校的，所以各位有精力的话也可以帮忙一起录入数据、为润学贡献一份自己的力量！

废话不多说，开始介绍排名方法。

---

# 排名方法

所有**原始数据**及其解释如下（均取编辑时最新数据）。

### 取自各大学的财务报表（Finance Statement）、年度报告（Annual Report）或官网统计（Number & Figure）的数据：

- **捐款（Donations, 简称 Dons）**：校友捐款、大学基金会等非补助非盈利性质的被动资金来源。这个指标可以间接反映一所大学的声誉和出路如何。比如说一所大学的捐款很多，可以说明这所大学的校友出路不错，不然没钱或者没面子捐钱，也可以说明校友对这所大学的评价很好，毕竟不喜欢的话为啥捐钱。反之，如果一所大学的捐款很少、忽略不计或者压根没有，除了以上的推测反过来之外，也有可能是这所大学就不存在捐款的传统。
- **财政拨款（Public Grants, 简称 Pub.Gs）**：政府层面的补助金，相当于办学经费。这个指标可以直接反映国家和当地政府层面对一所大学的重视程度。大手的智慧无需多言。
- **学费（Tuition Fees, 简称 T.Fees）**：这里的学费不止指单纯的学费，还包含注册费等等一切大学直接取自学生钱包的费用，是广义上的学费。评价是爆学生金币爆的。
- **总收入（Total Income, 简称 Total.I）**：值得说明的是，这项排名中统一用欧元计算总收入，汇率取编辑时最新汇率。
- **学术人员（Academic Staff, 简称 Ac.Staff）**：总雇员去除行政管理人员后负责科研和教学的人员。值得说明的是，这里不是单纯的计算人头数，而是使用FTE（Full Time Equivalent）计算。这个算法是更加科学的算法，会将兼职人员等进行加权计算，详细可见[维基百科](https://en.wikipedia.org/wiki/Full-time_equivalent)。当然，不是所有大学都会采用FTE计算，若是没有的话就采用人头数代替。
- **学生（Student, 简称 Stu）**：统计时在校总学生数，包含**博士生（PhD Student）**。

### 取自各大学科研论文发表统计相关的数据：

- **NIS（Nature Index Share）**：自然杂志根据一所大学的发文量和发文作者数加权计算得出的分数。这个指标可以大致反映一所大学在自然科学领域的科研总实力，详细可见 [Nature 官网](https://www.nature.com/nature-index/institution-outputs/generate/all/regions-Europe/all)。
- **CSRC（CS Rankings Count）**：取自 CS Rankings，这里取编辑时近10年数据。这个指标可以大致反映一所大学在计算机科学领域的科研质量，详细可见 [CS Rankings 官网](https://csrankings.org)。
- **CSRF（CS Rankings Faculty）**：取自 CS Rankings，这里取编辑时近10年数据。这个指标可以大致反映一所大学在计算机科学领域发过文章的科研人员数量，详细可见 [CS Rankings 官网](https://csrankings.org)。

额外提及一点，就是还有一个用于调参的数值是**回归系数（Regression Coefficient, 简称 R）**。这个数值用于将一项基于所有参与排名的大学的指标的平均数调到比如说 50.00 之类，如此一来可以防止在计算总分时某项指标得分过高或过低导致总分失真的情况发生。

---

以上是所有原始数据。各项**二级数据**及其解释如下：

---

## 声誉（Reputation, 简称 Rept）

一所大学的声誉由以下公式计算得出：

### **Rept = (Pub.Gs + Dons) / (Pub.Gs + T.Fees)**

如何理解这个公式？

首先，需要介绍一个新概念叫**金字塔模型**。灵感来源于[知乎一名答主的一篇回答](https://www.zhihu.com/question/268227369/answer/3283970953)。

金字塔模型指由捐款（Dons）、财政拨款（Pub.Gs）和学费（T.Fees）三项指标依次自顶向下排列组成的模型。很好理解的是，如果这个模型是个正金字塔，也就是当 Dons ＜ Pub.Gs ＜ T.Fees 时，说明这所大学的性价比很低、得到的回报远远比不上学生付出的金钱；反之，当 Dons ＞ Pub.Gs ＞ T.Fees 时，比如 ETH Zurich（2023）的 Dons 为 132,000,000 CHF、Pub.Gs 为 1,365,000,000 CHF 而 T.Fees 为 37,000,000 CHF，Dons 是 T.Fees 的四倍左右，那么可以近似视作一个倒金字塔，就说明这所大学的性价比很高、很值得读、回报付出比很高。反例比如 Uni Oxford（2023）的 Dons 为 ￡183,700,000、Pub.Gs 为 ￡229,200,000 而 T.Fees 为 ￡504,200,000，Dons 只有 Pub.Gs 的二分之一且只有 T.Fees 的四分之一，呈正金字塔型，反映出其付出回报比低。

在理解了金字塔模型的概念后，这个计算声誉的公式也就很好理解了。这个公式的目的是得出三个变量之间的一个比例数值，而作者数学水平有限，只得设计出如此公式。大致设计思路就是计算出 Dons 和 T.Fees 的比值，然后为了防止出现免学费（导致比值无穷大）或者没有捐款但财政拨款很高（没有捐款传统导致捐款少，但政府很重视）之类的情况出现，在除式两边各加了一次 Pub.Gs 来调和比例。

再然后还有一种加了对数处理后的公式：Rept = Log ((Pub.Gs + Dons) / (Pub.Gs + T.Fees) + 1, R) 。这里使用了以 R 为底的对数处理以消除边际效益的影响并进行调参，而前项的 + 1 是为了防止在进行对数处理时出现自参数小于 1 导致出现负数的情况。

那么最后看看实际效果如何：

- Uni Bocconi (2023): Rept = Log ((€ 12,600,000 + € 5,500,000) / (€ 12,600,000 + € 219,892,056) + 1, 1.008728) = 9
- Uni Oxford (2023): Rept = Log ((￡229,200,000 + ￡183,700,000) / (￡229,200,000 + ￡504,200,000) + 1, 1.008728) = 51
- VU Amsterdam (2022): Rept = Log ((€ 473,310,000 + € 0) / (€ 473,310,000 + € 60,361,000) + 1, 1.008728) = 73
- DTU (2022): Rept = Log ((2,802,082,000 kr. + 0 kr.) / (2,802,082,000 kr. + 85,816,000 kr.) + 1, 1.008728) = 78
- ETH Zurich (2023): Rept = Log ((1,365,000,000 CHF + 132,000,000 CHF) / (1,365,000,000 CHF + 37,000,000 CHF) + 1, 1.008728) = 84

以及极端情况：

- 正金字塔型：Rept = (1,000 + 0) / (1,000 + 1,000,000) = 0.001
- 菱形：Rept = (1,000,000 + 0) / (1,000,000 + 0) = 1
- 倒金字塔型：Rept = (1,000 + 1,000,000) / (1,000 + 0) = 1000

那么关于 Rept 就说明到这里，简而言之就是一个关乎性价比的指标，富哥可略。

## 教学（Teaching, 简称 Tng）

一所大学的教学由以下公式计算得出：

### **Tng = (Ac.Staff / Stu) * (Total.I / Stu)**

这个公式可以拆为两个部分，也就是**师生比（Ac.Staff / Stu）**和**学生人均资金（Total.I / Stu）**。很好理解，所以不多赘述。还有一种加了对数处理后的公式，可参见上文。

那么看看实际效果如何：

- Open Uni UK (2022): Tng = Log ((3255 / 151840) * (€ 648,180,000 / 151840), 1.1755) = 28
- PoliMi (2022): Tng = Log ((1627 / 47959) * (€ 582,806,128 / 47959), 1.1755) = 37
- Uni Copenhagen (2022): Tng = Log ((5809 / 27380) * (€ 1,253,200,000 / 27380), 1.1755) = 57
- Scuola Superiore Sant'Anna (2022): Tng = Log ((393 / 819) * (€ 76,603,690 / 819), 1.1755) = 66

以及极端情况：

- 双高：Tng = (1 / 1) * (€ 1,000,000 / 1) = 1000000
- 师生比高而学生人均资金少：Tng = (1 / 1) * (€ 1,000 / 1) = 1000
- 师生比低而学生人均资金多：Tng = (1 / 1000) * (€ 1,000,000,000 / 1000) = 1000
- 双低：Tng = (1 / 1000) * (€ 1,000,000 / 1000) = 1

那么关于 Tng 就说明到这里，简而言之就是一个关乎体验和质量的指标，衡水式教育爱好者可略。

## 教育（Education, 简称 Edu）

一所大学的教育由以下公式计算得出：

### **Edu = (Rept + Tng) / 2**

也很好理解，其实就是 Rept 和 Tng 的平均数，所以不多赘述。

这里说明两种特殊情况。

1. Rept 高但 Tng 低：我愿称之为典型的放养式教育，很适合草根出身的贫民。当然常规情况下 Rept 高但 Tng 低是不如双高的，只是说竞争一般没那么激烈、性价比拉满了。可以发现，德国的大学其实就属于这种类型——不收学费、门槛低，但是体验和质量只能说是一言难尽......
2. Rept 低但 Tng 高：属于是贵族学校了，适合金币多的富蛆和去镀金的小瘤。同上，低性价比会劝退很多人，所以竞争一般也没那么激烈。可以发现，英国的大学其实就属于这种类型——体验和质量很不错，但是成本......懂得都懂。

---

如果纯读书不看科研的话，到这里已经可以不用继续往下看了，因为往下都是考虑科研实力的指标。

---

## 自然科研（Nature Science Research, 简称 NSR）

一所大学的自然科研由以下公式计算得出：

### NSR = NIS / Stu

很好理解，其实就是一所大学的学生人均在自然科学领域的发文量的一个指标，所以不多赘述。还有一种加了对数处理后的公式，可参见上文。

## 计算机科研（Computer Science Research, 简称 CSR）

一所大学的自然科研由以下公式计算得出：

### CSR = (CSRC * CSRF) / Stu

这个公式先是拿 CSRC 乘以 CSRF 算出了一所大学的总发文量，然后再除以学生人数，得到的一所大学的学生人均在计算机科学领域的发文量的一个指标。还有一种加了对数处理后的公式，可参见上文。

---

以下是总分指标，如果既读书也做研究的话可以多参考以下指标。当然，如果纯读书或者纯做研究的话建议还是参考前面的 Edu、NSR 或者 CSR。

---

## 自然科学综合（Nature Science Total, 简称 NST）

一所大学的自然科学综合由以下公式计算得出：

### NST = (Rept + Tng + NSR) / 3

这个公式很好理解，不多赘述。这个指标是综合考虑了 Rept、Tng 和 NSR 的结果，也就是教研结合的最终分数。

那么看看实际效果如何（自参数经过对数处理）：

- EPFL (2023): NST = (80 + 64 + 217) / 3 = 120
- Aarhus University (2022): NST = (79 + 55 + 71) / 3 = 68
- Uni Manchester (2023): NST = (25 + 51 + 42) / 3 = 39

## 计算机科学综合（Computer Science Total, 简称 CST）

一所大学的自然科学综合由以下公式计算得出：

### CST = (Rept + Tng + CSR) / 3

同上。实际效果（自参数经过对数处理）：

- IT Uni Copenhagen (2022): CST = (78 + 51 + 593) / 3 = 241
- TU Delft (2022): CST = (73 + 56 + 120) / 3 = 83
- Uni Padova (2022): CST = (68 + 57 + 15) / 3 = 47

## 自然&计算机科学综合（Nature & Computer Science Total, 简称 NCST）

一所大学的自然&计算机科学综合由以下公式计算得出：

### NCST = (NST + CST) / 2

那么看看实际效果如何（自参数经过对数处理）：

- Uni Cambridge (2023): NCST = (118 + 66) / 2 = 92
- TU Eindhoven (2022): NCST = (66 + 56) / 2 = 61
- UCL (2022): NCST = (27 + 44) / 2 = 36

适合给那些电子工程、生物信息之类专业的学生参考，也就是既得考虑自然科学也得考虑计算机科学。

---

以上就是排名方法的介绍了。不要问我为什么不考虑社会科学等等却只考虑理工科。如果是考虑社科之类的话，个人推荐是采用 [Uni Leiden 的 CWTS](https://www.leidenranking.com/ranking) 中的参数，然后自行魔改。

### 注：自 2024 年 4 月 8 日更新后，排名的算法大幅改动、引入了标准差，但大致思路同为消除某一个指标过于极端的影响。

---

# 共享说明

文件是采用 Excel 的形式，也有供在线查看、编辑的 CSV 格式。下载后默认是按照 NCST 排名的情况，自行查看、对比各院校数据即可。

如果想为此项目贡献一份力的话，请根据表格模式添加完院校（查不到的数据留 *，然后二级数据处取 100（平均数）并标红）后确保表格右侧 Average 四项数值为 100.00（使用数据分析工具）。这就是上方的 R 计算出的平均值。总之就是添加完后可以帮忙微调 R，至于如何调整可以参考[知乎的这篇回答](https://zhuanlan.zhihu.com/p/521218910)。在处理完之后正常提交，**记得在备注栏填写所用数据的来源（链接形式）**、警告（存疑点）和使用的汇率。

感谢各位的支持和参与！

---

# 项目进度

以统计完全上榜 CS Rankings 或 Nature Index Share 大于等于 1.00 的院校为标准：

- [x] 瑞士（CH）
- [x] *比利时（BE）
- [x] 荷兰（NL）
- [x] 丹麦（DK）
- [x] 爱沙尼亚（EE）
- [x] 拉脱维亚（LV）
- [x] 立陶宛（LT）
- [x] 卢森堡（LU）
- [x] 冰岛（IS）
- [x] 芬兰（FI）
- [x] *挪威（NO）

*部分院校数据缺失

---

Shield: [![CC BY 4.0][cc-by-shield]][cc-by]

This work is licensed under a
[Creative Commons Attribution 4.0 International License][cc-by].

[![CC BY 4.0][cc-by-image]][cc-by]

[cc-by]: http://creativecommons.org/licenses/by/4.0/
[cc-by-image]: https://i.creativecommons.org/l/by/4.0/88x31.png
[cc-by-shield]: https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg
