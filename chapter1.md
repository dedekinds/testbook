# Machine Learing?

### 1.什么是学习？什么是机器学习？

李航所著的《统计学习方法》中开篇有一句话定义了“学习”，

“如果一个系统能够通过执行某个过程**改进它的性能**，这就是学习”——Herbert A.Simon

![](/assets/3WS0M%28LF_E}D_{%29~E6P%28@Q7.png)

### 2.机器学习的可行性

在学习这一部分的时候，我们知道实际上$$f$$是未知的，是不能知道的，这是一个前提假设，按林老师的说法就是，如果知道了$$f$$那我们还玩什么呢？我们不过实在hypothesis set 中通过learning algorithm来找到一个最好的$$h$$，我们称为$$g$$去逼近$$f$$,由此我联想到了三点：

* 有点像**缸中之脑**的情况，永远无法判断自己所看到的世界（$$g$$），是否是世界原来本身（$$f$$）的面目。

* 大概3年前思考了如下问题：如何判断一个**密码被正确破译**呢。一段足够复杂的明文加密后能被破译成两种棒棒哒的意思呢?如果可以。能构造出来吗？[https://tieba.baidu.com/p/3252833201](https://tieba.baidu.com/p/3252833201)

* 在周志华的《机器学习》P8中有讲到**没有免费午餐定理**，这在林的课程后面也有讲到：

对于一个学习算法$$A_a$$，若它在某些问题上比学习算法好$$A_b$$，则必然存在某些问题，在那儿算法$$A_b$$比算法$$A_a$$要好。

即考虑样本空间$$\mathcal{X}$$和假设空间$$\mathcal{H}$$都是离散的，用$$P(h|X,A_a)$$来表示算法$$A_a$$基于训练数据$$X$$产生假设$$h$$的概率，那么算法在训练集以外的误差为：（主要我们看的是在训练集外的性能，成为泛化性）


$$
E_{ote}(A_a|A,f)=\sum_h\sum_{x\in \mathcal{X}-X} P(x)\cdot I(h(x)\neq f(x))P(h|X,A_a)
$$


可以证明在$$f$$满足均匀分布的时候，有$$\sum_f E_{ote}(A_a|X,f)=\sum_f E_{ote}(A_b|X,f)$$。

在林轩田的课程里用了这个例子：

![](/assets/5CRW6R1QEIR8{XXQ5%28@4_3F.png)

[http://beader.me/mlnotebook/section2/is-learning-feasible.html ](http://beader.me/mlnotebook/section2/is-learning-feasible.html)中的2.1节对此描述很详细

