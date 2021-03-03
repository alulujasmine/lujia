# Welcome to Jia Lu's HomePage!　
# 欢迎来到路佳的个人主页！

I am a graduate student majored in astrophysics. 

And this is the latest version of [my CV](https://www.overleaf.com/read/rpvywxzbtmtw).

我最新版本的简历可见于：[my CV](https://www.overleaf.com/read/rpvywxzbtmtw).


I plan to share some of my feelings and experience during my research and some popular science articles and scientific fiction stories (Coming soon!) by myself here.

我打算在这里记录、分享一些自己的研究过程中的经历、收获和感想，同时也会放一些自己创作的科普小文、科幻故事（敬请期待！）。

The Content is (目录为)：

**Research Experience**

**Research Feelings and Popular Science**

**Scientific Fiction**

**Hobbies**


## Research Experience

### Master Dissertation 
High Reshift Type Ia Supernovae on Cosmological Parameter Estimation and Model Selection
(Paper in preparation)

### Cosmology Course Final Project 
[The CMB Temperature Power Spectra with Varying Dark Energy of State w](https://github.com/jasminelujia/AY15206CosmoFinal)

### Journal Club Talk 
[the standard siren measurement of Hubble constant](https://github.com/jasminelujia/standard_siren_H0)

### Bachelor Thesis 
[The Technology Systerm of River Wetland Restoration -- Huxi River as a Case Study](https://github.com/jasminelujia/BachelorThesis)

### Professional Internship 
[Professional Internship in Waste Treatment and Disposal Centers and Industries](https://github.com/jasminelujia/ProInternsh.EnviScience)

### Term Paper
[Environmental Impact Assessment of Electroplating Production Lines ](https://github.com/jasminelujia/TermPaper-EIA)


## Research Feelings and Popular Science

### **学习统计推断时的自问自答**

##### 1.参数估计
###### Q1: minimum method 和maximum likelihood estimation的区别是什么？

A1：least square method是maximum likelihood method的一个special的分支。当likelihood为Gaussian时， least square method和maximize likelihood一样。

refs：
1. Data Reduction and Error Analysis for Physical Science
2. On Model Selection in Cosmology
3. lectures on cosmology


###### Q2：maximum likelihood方法与Bayesian方法中的likelihood的区别是什么？
A2：两者的likelihood的表达式都是p(d|theta)(其中为d数据，为theta参数)。
maximum likelihood 方法中的likelihood被视为参数的函数，是人为可调的。我们选择使likelihood最大的参数值作为最佳参数值；
Bayesian方法中的likelihood是通过观测数据得到的，不是人为可调的。我们通过对真实数据的观测得到likelihood；根据经验或其它原则（此处有不同观点，参见Mathematical Statistics and Data Analysis 3rd - John Rice）确定参数的先验分布；最后，根据Bayes定理，得到参数的后验分布。

refs:
1.Maximum Likelihood vs. Bayesian Parameter Estimation Ronald J. Williams CSG 220 Spring 2007
2.What is the difference in Bayesian estimate and maximum likelihood estimate? - StackOverflow

###### Q3: maximum likelihood 方法中选择使likelihood最大的参数值作为最佳参数值。从这种表述看，似乎得到的是确定的参数值，那么文献中出现的参数值的概率分布图是如何得到的？
A3：因为我们想知道测量参数的误差

ref: emcee manual

##### 2.chi2一家子
1.chi2分布
2.minimum chi2 方法
3.chi2统计量-goodness of fit

(待补充......

##### 3.data和model之间不得不说的故事
###### Q：用data去constrain model的参数和fit a model to data的区别是什么？

A：前者是模型已经存在，人们通过数据对模型的参数进行限制；后者是先得到了数据，人们去建立模型或者拿已有的模型去fit(解释)它。
前者可以用Bayesian方法，后者可以用maximum likelihood方法。


### **程序求解数独的思路**
2019-02-21 16:42:06

第一种：
1.读取方格，检测是否已存在数字，循环81(方格的总数)次。记录下空格的数量N和位置(xi,yi)（i=1～N）；
2.每个空格(xi,yi)的备选数字为0-9，一共10种可能。N个空格，存在10^N种数字组合，即10^N种填法；
3.填入一种组合，检验是否合适。是，则完成；否，则填入下一种组合，循环直到满足要求。
这种方法思路比较简单，但可能会比较慢。

第二种：
1.读取方格，检验是否已存在数字。记录下已存在的数字c(c=0~9)与位置(xi,yi)。循环完毕，记录下空格的数量N，则已存在的数字总数为81-N；
2.已存在数字ci所在行、列、九宫格的空格可填入的数字为非c。记每个空格所在的行、列已有的c的数量为m，则每个空格可填入的选择有(10-m)种。总体一共有(10-m)^N种填法；
3.填入一种组合，检验是否合适。是，则完成；否，则填入下一种组合，循环直到满足要求。
这种思路稍微复杂一点，逻辑和人填数独的思路相近。由于(10-m)小于10，似乎应该会更快一点，但是可能也不一定。也许可以计算一下m，看在什么范围下第一种方法比较快，什么范围下第二种方法比较快，什么情况下两者一样。

在知网搜索了一下“数独”，在arXiv搜索了一下“sudoku”，发现已有的相关研究还挺多的。
中文文献可以帮助对于非此研究领域专业人士的爱好者在短时间内了解研究的意义和应用领域、研究的发展历史和现状；英文文献则可以有助于了解目前国际上该领域的学者所关心的问题和研究的现状。（2019年4月29日）

翻了一下《Python科学计算》，发现682页给出了一个程序求解数独的实例。 
(无关的话：因为打算卖掉这本书而翻了一下，却有意外收获，也算很意外了吧……


### **学习天文学的个人感想**
2018.01.23 20:40:50 

根据研究内容来分类。按照研究对象的尺度从小到大的顺序，天文学的研究方向包括：行星科学、恒星与分子云、高能天体物理现象、星系大尺度结构、宇宙学。行星科学与地球科学有较多交叉，宇宙学与物理学有相对较多的交叉。
根据研究方法来分类。天文学研究的方向包括观测、理论、数值模拟、仪器技术。

观测研究者要做的事情是获取有价值的信息。具体操作上来说，要知道怎么做(how)，比如说，如何选择观测目标、如何实现观测过程、如何获得观测数据、如何处理得到的观测数据；然后指出是什么(what)，即阐明观测的结果。

理论研究者是要做的事情是解释已有的观测结果(why)、预言可能出现的观测现象、帮助确定观测目标和计划。解释观测现象的理论可以有很多，区分它们的关键有：1.与现有观测数据的符合程度(goodness  of fit)；2.模型的复杂程度，根据奥卡姆剃刀原理，自然是越简单越好；3.预言的现象能否被观测证实。
数值模拟是一种用计算机模拟真实情况的方法。它的出现的原因有：1.观测的限制。首先，望远镜的观测时间有一定限制；其次，望远镜的建设需要较高的成本；以及，望远镜技术（精度、口径等）存在限制。2.研究对象的特殊性。以宇宙为例：只存在一个宇宙，我们无法拿它与同类研究对象对比；宇宙的演化过程不可重复，我们无法真实再现这一过程。（除非新创建一个宇宙？emmm,  good idea for science  fiction）如果我们想研究宇宙演化过程中的现象或机制，除了从观测数据中获取信息，我们还可以用计算机模拟演化过程，比如，给出初始条件和演化规律，推算演化结果。

仪器技术方面。目前比较成熟的是采用电磁波作为观测窗口的望远镜，其观测波段从长到短可以分为：射电、红外、光学、紫外、X射线、Gamma射线。除以电磁波作为观测窗口的望远镜 ，还有探测引力波的望远镜，比如著名的Ligo、Virgo。但是目前它们的主要任务是去发现引力波，而不是用引力波作为窗口去探测、研究其它的天体物理现象、宇宙学现象等。根据观测地点的不同，望远镜可以分成地基望远镜和太空望远镜，后者比如著名的哈勃太空望远镜。地基望远镜一般会建在人烟稀少、光污染少、空气稀薄的地方，比如南极、南非沙漠、智利、青海、西藏。
 
2019.1.29
一年前写了第一版，现在又有了新感想，来修改一下。现在感觉以前写的东西像shi一样，而当时写完后似乎是很得意的，啊捂脸。不过这至少说明自己还是进步了的。也许“后之视今亦如今之视昔”吧，加油。

2020.10
之前放在别的地方了，现在搬过来。补上了一点关于仪器的内容。想了一想，写下来的似乎都是常识性或者说知识性的东西，即，可以直接在一本导论书里或者维基百科里到看的东西。当时写下来，大概也是因为学到一点什么而迫不及待想说出来？不，大约只是闲得慌而已。当作一个记录好了。


### **学物理时的收获与感想**
2018-02-02 12:24:58

我们为什么存在？

因为正反物质不对称。（参考文献：向守平《天体物理概论》P292）

感想： 物理学回答的这个问题很像哲学问题。


    第三片中的粒子……在进入黑洞后，落入奇点前，它也可能与来自第一片的粒子相遇。但是，它们所交流的信息是送不回第一片或第三片的。因此，这两片是完全隔绝的。

（引自俞允强《广义相对论引论》P119）

感想：这段话的感觉很像科幻小说。“完全隔绝”，有一种宿命的决绝与哀伤。

黑洞的热容是负的，也就是说：它吸收能量，结果是温度减低；它放出能量，温度升高。
如果黑洞的初始温度大于环境温度，它将通过辐射而放出热量。由于热容为负，它的温度会升高，从而它将继续辐射热量直到能量耗尽；
如果黑洞的初始温度小于环境温度，它将从环境吸收能量。由于热容为负，它的温度将降低，从而持续从环境中吸收热量。
如果只考虑热辐射，不考虑非热过程，那么黑洞演化的结局只有两个极端：完全消失或者越长越大。
（参考文献：俞允强《广义相对论引论》P127-P128）

感想：黑洞真是一种神奇的存在。

为什么它的热容为负呢？
这是由它的能量与温度的关系式得来的。它的能量与温度的关系式从何推来的呢？由Hawking的黑洞动力学第二定律（面积不减定理）与Berkenstein的熵与面积关系以及黑洞能量（质量）与态变量的热力学关系得来的。黑洞的面积如何算出来的呢？由Kerr-Newmann黑洞的视界半径。Kerr-Newmann黑洞的视界半径如何来的呢？由Kerr-Newmann度规。Kerr-Newmann度规是如何来的呢？它是Einstein场方程的一个轴对称解。Einstein场方程是如何来的呢？它来自Einstein的脑中（开个玩笑），它也来自在此之前很多人如Gauss，Minkowski，Riemann，Poincaré等的工作。把这个说清楚需要很长的篇幅，应该属于广义相对论早期的发展历史。
再扯回来，从另一方面说，热容是物质的属性，所以它热容为负是因为它天生如此。为什么它天生如此呢？不知道，就像我不知道花儿为什么天生如此叶子为什么天生如此人为什么天生如此
为什么为什么为什么？
问出为什么是不是就是科学的开始呢？
然后寻找答案给出答案是科研？

2018.02.04补充：
和办公室的人交流了一下黑洞的性质。有人问了一个问题：黑洞是如何辐射热量的？一下被问住了。wiki了一下radiation，链接到了Hawking radiation，与量子效应有关。又回到俞允强的书，发现在推导黑洞的热容之前，书中已经给出黑洞的辐射机制的说明了，现摘录如下:

    1974年霍金指出，黑洞的辐射可以通过量子效应来实现。黑洞表面附近的真空涨落产生虚粒子对，当其中负能虚粒子通过隧道效应而进入黑洞，黑洞的能量将减少，同时其中的正能粒子可能向外穿出黑洞的外引力区，这相当于黑洞辐射了一个粒子。这种机制被称作霍金辐射。
    
这个插曲大概是告诉我独学而无友则孤陋寡闻？
    

### My Way of Programming
2018-07-23 21:40:24

最早接触编程是在大学的时候，大二上学期选修C程序设计课程。（或者严格一点说是高中时数学课上学习算法结构？）当时，理论课上，我因为倍觉枯燥而没有认真听课，课下也没有温习，于是听不懂老师讲的课了；实验课上，也多半是复制老师给的源代码然后稀里糊涂的运行。期末考试前我才着了慌，熬夜到凌晨三点，才勉强没有挂掉。大二下学期，周围很多同学报名考计算机二级C，我也报名了。这时候，我开始系统性地学习了一下C语言，主要是看书、练习。后来二级考过了，分数比C程序课程的期末成绩还好很多。再后来，一直到本科毕业，我没有遇到需要使用编程的情况，C也渐渐生疏了。

大四的时候，我打算跨专业考研，去读物理。后来读了天体物理。研一下学期，一些专业课需要用编程来解决问题。我想起以前学习C语言的痛苦经历，完全不想去碰编程。最后，因为很多作业需要编程来解决，我不得不学了一点python。

研二上学期，我开始接触课题。很多东西都需要用到编程。我开始系统地学习python，用的书是《Python编程：从入门到实践》，我跟着书上的课程一步一步的学习，竟感觉非常轻松。后来，看了一点《LaTeX入门》，当我成功地输出第一个pdf文件时，心里有一点兴奋。渐渐地觉得不那么讨厌编程了，因为它很准确（错了一个字母甚至标点都可能导致bug）、很忠诚（只要输入正确的命令，它就能执行出你想要的结果）。

寒假的时候，去图书馆，无意中看到了《Mathematica与大学物理计算》这本书，觉得很好奇，加之本科时旁听物理系的课程，老师提到过mathematica，我于是借了一本书回去看。下载了mathematica试用版，边看书边学习。发现mathematica非常简单，其语言形式和自然语言很像，数学表达式也和书本上的自然表达式几乎一致。我很开心地学了一段时间，直到15天试用期结束= =。书内还有一些作者对物理的思考与体会，比如：被物理的”美貌“吸引，进来之后才发现完全不是如此；我们将实际问题抽象成物理模型，我们对问题的解答实际上是对模型的解答，未必是对真实物理状态的解答，“中间的差别大小取决于模型接近真实系统的程度”……让我觉得很受启发。

两个星期前，我旁听了“天文统计学与R语言”暑期学校的课程。这是我读研以后第一次系统地去学习编程类课程（学校开了“Linux系统和IDL”的课程，我当时觉得不感兴趣而没有选= =），感觉R语言和mathematica很像，学起来也很开心。

现在，因为经常使用，编程似乎成了一件很日常的事情。有时候，我觉得，敲几行字母，就能画出超棒的图形；给几个命令，系统却type出一大串，编程是一件很酷的事情。有时候，我觉得，编程好无趣、枯燥、没有感情、没有美感，我不想作程序yuan。（关于美感这一点，高德纳是认为编程是一种艺术的。也许，我还没有到能体会到美感的水平；也许，我就是觉得这件事情枯燥，跟水平无关。）


### _Memories of a Theoretical Physicist_ 阅读笔记与感想
2018-02-05 20:34:32

之前看到有人推荐这篇文章Memories of a Theoretical Physicist ，作者Joseph Polchinski。今天看微信文章，才知道他于2月2号因病去世了。
今天把文章下载了下来，开始读了，发现了一些有趣的地方。
P9：章节名：1 Early years

    The next year, I took Advanced Algebra……It was taught by the football coach

真·数学是体育老师教的（= =开个玩笑）

P21-22：章节名：2 Caltech，1971-1975

    I remember spending a few hours moving some lead blocks with Tom, and thinking I did not want to spend my career moving lead blocks.

“move lead blocks”，是不是可以翻译成搬砖？= =

P23：章节名：2 Caltech，1971-1975

    Another source of particle physics excitement was the discovery of a new long-lived heavy particle J/ψ, something that had not been seen before……Glennys Farrar, proposed that it was a bound state of thecharmed quark with its antiquark. Fairly quickly, the latter was confirmed.

Bing了一下Glennys Farrar，原来是一位女物理学家！她于1971年在普林斯顿获得理论物理博士学位，“ breaking the gender-barrier in physics at Princeton in the process”，当真是我的榜样！

P24：章节名：2 Caltech，1971-1975
Murray Gell-Mann
从维基百科上链接到了他的个人主页 ，第一眼觉得老爷爷真慈祥啊！
然后看到了照片右边的研究领域：Cosmology（宇宙学），The Evolution of Human Languages（人类语言的演化），Quantum Mechanics（量子力学），Regularities in Human History（人类历史的规则性）。“Publication”里列出的最新的论文是2009年发表在Journal of Language Relationship上面的一篇语言学论文，老爷子是一作。
以前听说，“夸克”名字的出处为James Joyce的Finnegans Wake（《芬尼根的守灵夜》），命名者即为Gell-Mann。现在看来，这位大师同赵元任一样，都是复合型的天才啊！

P34:章节名：3 Berkeley，1975-1980

    After five years, it was time to write a dissertation.  In theoretical physics,the  custom  was  simply  to  combine  one’s  published  papers,  often  written with  one’s  advisor  or  others,  and  insert  some  amount  of  overview.   But  I had a problem:  I had written no papers at all (the undergrad papers under Tombrello didn’t count). This is extremely rare. ......  I  was  simply  suffering  from  a  lack  of common  sense  and  of  any  collaborative  instinct,  and  an  advisor  who  wasmuch the same. Somehow I cobbled together 130 pages about what I had understood about vortex operators, and related issues of field theory.

大牛临近毕业时也没有文章......我的焦虑感稍稍减轻了一点......

P35: 章节名：4 SLAC/Stanford，1980-1982
这一章主要讲作者在SLAC作博士后的经历。其中有一些内容是关于作者的研究内容的，如超对称、D-terms、对称破缺等等，非专业人士看起来可能会有些费解。

2018年10月21日:终于看完了，断断续续。正如作者自己在结尾所言，在物理学领域他几乎是走一条直线（“taken a rather linear path”），没有旁枝末节（“with few deviations”），我想这大概是指他没有想过去从事其它事业吧。从最初的由科普书（“How and Why Wonder Books”）引起兴趣，到后来从事科学研究，他没有实现早期的创作科幻作品的愿望（“my early science fiction goals”），也没能回答“why there is something rather than nothing”，但他确实在基础科学领域作出了自己贡献（“had an impact on the most fundamental questions of science”）。


## Scientific Fiction
Coming soon !



## Hobbies
[Drawing](https://github.com/alulujasmine/MyPaintings)

Reading

Gardening

Running

TableTennis





