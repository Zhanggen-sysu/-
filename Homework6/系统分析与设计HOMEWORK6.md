# 系统分析与设计HOMEWORK6

### 一、简答题

1. 用例的概念

   用例是软件工程或系统工程中对系统如何反应外界请求的描述，是一种通过用户的使用场景来获取需求的技术。每个用例提供了一个或多个场景，该场景说明了系统是如何和最终用户或其它系统互动，也就是谁可以用系统做什么，从而获得一个明确的业务目标。

2. 用例和场景的关系？什么是主场景或 happy path？

   - 用例是一组相关的成功和失败场景的集合 ，这些场景描述了业务参与者使用系统实现一个业务目标的过程。
   - 场景是业务参与者和系统之间的一系列特定的活动和交互，也叫用例实例。场景是使用系统的一个特定情节或用例的一条执行路径。
   - 主场景：也被称为“理想路径”场景，或更朴实的“基本流程”及“典型流程”。它描述了满足涉众关注点的典型成功路径。在该场景中，主执行者完成了目标，所有项目相关人员的利益都被满足。它通常不包括任何条件或分支，保持了一定的连贯性，将所有条件处理都推延至扩展部分。

3. 用例有哪些形式？

   - 摘要——简洁的一段式概要，通常用于主成功场景，在早期需求分析过程中，为了快速了解主题和范围可能会用到。
   - 非正式——非正式的段落格式。用几个段落覆盖不同场景。和摘要一样，只应用在早期需求分析过程中。
   - 详述——详细编写所有步骤及各种变化，同时具有补充部分，如前置条件和成功保证。在确定并以摘要形式编写了大量用例后，在第一次需求讨论会中，需要详细编写其中少量的具有重要架构意义和高价值的用例。

4. 对于复杂业务，为什么编制完整用例非常难？

   复杂业务涉及到的场景很多且复杂，在编制用例时可能会遗漏一些细节甚至因考虑不周到出现错误，所以编制完整用例非常难。

5. 什么是用例图？

   用例图是指由参与者（Actor）、用例（Use Case），边界以及它们之间的关系构成的用于描述系统功能的视图。用例图（User Case）是外部用户（被称为参与者）所能观察到的系统功能的模型图。用例图是系统的蓝图。用例图呈现了一些参与者，一些用例，以及它们之间的关系，主要用于对系统、子系统或类的功能行为进行建模。

6. 用例图的基本符号与元素？

   - 参与者：参与者不是特指人，是指系统以外的，在使用系统或与系统交互中所扮演的角色。因此参与者可以是人，可以是事物，也可以是时间或其他系统等等。还有一点要注意的是，参与者不是指人或事物本身，而是表示人或事物当时所扮演的角色。
     - 参与者在画图中用简笔人物画来表示，人物下面附上参与者的名称。
     - ![1555559788440](https://github.com/Zhanggen-sysu/Software-Analysis-Design-Homework/raw/master/Homework6/1.png)
   - 用例：用例是对包括变量在内的一组动作序列的描述，系统执行这些动作，并产生传递特定参与者的价值的可观察结果。用例是参与者想要系统做的事情。
     - 用例在画图中用椭圆来表示，椭圆里附上用例的名称。
     - ![1555559810712](https://github.com/Zhanggen-sysu/Software-Analysis-Design-Homework/raw/master/Homework6/2.png)
   - 系统边界：系统边界是用来表示正在建模系统的边界。边界内表示系统的组成部分，边界外表示系统外部。
     - 系统边界在画图中用方框来表示，同时附上系统的名称，参与者画在边界的外面，用例画在边界里面。
     - ![1555559966597](https://github.com/Zhanggen-sysu/Software-Analysis-Design-Homework/raw/master/Homework6/3.png)
   - 箭头：箭头用来表示参与者和系统通过相互发送信号或消息进行交互的关联关系。箭头尾部用来表示启动交互的一方，箭头头部用来表示被启动的一方，其中用例总是要由参与者来启动。
     - 关联：表示参与者与用例之间的通信，任何一方都可发送或接受消息。
       - 【箭头指向】：无箭头，将参与者与用例相连接，指向消息接收方。
       - ![1555560543965](https://github.com/Zhanggen-sysu/Software-Analysis-Design-Homework/raw/master/Homework6/4.png)
     - 泛化：就是通常理解的继承关系，子用例和父用例相似，但表现出更特别的行为；子用例将继承父用例的所有结构、行为和关系。子用例可以使用父用例的一段行为，也可以重载它。父用例通常是抽象的。在实际应用中很少使用泛化关系，子用例中的特殊行为都可以作为父用例中的备选流存在。
       - 【箭头指向】：指向父用例
       - ![1555560601617](https://github.com/Zhanggen-sysu/Software-Analysis-Design-Homework/raw/master/Homework6/5.png)
     - 包含：包含关系用来把一个较复杂用例所表示的功能分解成较小的步骤。包含关系对典型的应用就是复用，也就是定义中说的情景。但是有时当某用例的事件流过于复杂时，为了简化用例的描述，我们也可以把某一段事件流抽象成为一个被包含的用例；相反，用例划分太细时，也可以抽象出一个基用例，来包含这些细颗粒的用例。这种情况类似于在过程设计语言中，将程序的某一段算法封装成一个子过程，然后再从主程序中调用这一子过程。
       - 【箭头指向】：指向分解出来的功能用例
       - ![1555560639895](https://github.com/Zhanggen-sysu/Software-Analysis-Design-Homework/raw/master/Homework6/6.png)
     - 扩展：扩展关系是指用例功能的延伸，相当于为基础用例提供一个附加功能。将基用例中一段相对独立并且可选的动作，用扩展（Extension）用例加以封装，再让它从基用例中声明的扩展点（Extension Point）上进行扩展，从而使基用例行为更简练和目标更集中。扩展用例为基用例添加新的行为。扩展用例可以访问基用例的属性，因此它能根据基用例中扩展点的当前状态来判断是否执行自己。但是扩展用例对基用例不可见。对于一个扩展用例，可以在基用例上有几个扩展点。
       - 【箭头指向】：指向基础用例
       - ![1555560714036](https://github.com/Zhanggen-sysu/Software-Analysis-Design-Homework/raw/master/Homework6/7.png)
     - 依赖：以上4种关系，是UML定义的标准关系。但VS2010的用例模型图中，添加了依赖关系，用带箭头的虚线表示，表示源用例依赖于目标用例。
       - 【箭头指向】：指向被依赖项
       - ![1555560756090](https://github.com/Zhanggen-sysu/Software-Analysis-Design-Homework/raw/master/Homework6/8.png)

7. 用例图的画法与步骤

   - **确定参与者** 
     在获取用例前首先要确定系统的参与者， 开发人员可以通过回答以下的问题来寻找系统的参与者。 

     （1）         谁将使用该系统的主要功能。 

     （2）         谁 将需要该系统的支持以完成其工作。 

     （3）         谁将需要维护、管理该系统，以及保持该系统处于工作状态。 

     （4）         系 统需要处理哪些硬件设备。 

     （5）         与该系统那个交互的是什么系统。 

     （6）         谁或什么系统对本系统产生的结果感兴趣。

   - **识别用例** 
     用例图对整个系统建模过程非常重要，在绘制系统用例图前，还有许多工作要做。系统分析者必须分析系统的参与者和用例，他们分别描述了“谁来做”和“做什么”这两个问题。识别用例最好的方法就是从分析系统的参与者开始，考虑每一个参与者是如何使用系统的。使用这种策略的过程中可能会发现新的参与者，这对完善整个系统的建模有很大的帮助。用例建模的过程是一个迭代和逐步精华的过程，系统分析者首先从用例的名称开始，然后添加用例的细节信息。这些信息由简短的描述组成，它们被精华成完整的规格说明。
     在识别用例的过程中，通过回答以下几个问题，系统分析者可以获得帮助。 

     （1）         特定参与者希望系统提供什么功能。 

     （2）         系统是否存储和检索信息，如果是，由哪个参与者触发。 

     （3）         当系统改变状态时，是否通知参与者。 

     （4）         是否存在影响系统的外部事件。 

     （5）         哪个参与者通知系统这些事件。

   - **识别用例间的关系**

     分析用例间是否存在关联，泛化，包含，扩展，依赖等关系，如果有，就用对应的箭头将用例连接起来。

8. 用例图给利益相关人与开发者的价值有哪些？

   - 对利益相关人：
     - 用例图可用于估计项目规模和复杂性，有助于项目预算的估算；
     - 用例图有助于确定系统的核心要求及其变体，有助于利益相关人在软件开发项目的生命周期早期阐明并改进这些要求。
     - 用例图可以有效地总结客户（参与者）与将为企业提供价值的系统之间所需的交互。
   - 对开发者：
     - 用例图可以帮助将大型系统划分为多个模块。每个模块本身可以由用例图表示，有利于开发者对系统功能需求的分解。
     - 用例图的边界特征有助于隔离系统的内部和外部元素，有利于开发者了解系统的核心功能。
     - 用例图可用来评估和确定需求的优先级，有利于开发者确定功能开发的先后顺序。

### 二、建模练习题（用例模型）

- 选择2-3个你熟悉的类似业务的在线服务系统（或移动 APP），如定旅馆（携程、去哪儿等）、定电影票、背单词APP等，分别绘制它们用例图。并满足以下要求：
  - 请使用用户的视角，描述用户目标或系统提供的服务
  - 粒度达到子用例级别，并用 include 和 exclude 关联它们
  - 请用色彩标注出你认为创新（区别于竞争对手的）用例或子用例
  - 尽可能识别外部系统和服务
- 然后，回答下列问题：
  1. 为什么相似系统的用例图是相似的？
  2. 如果是定旅馆业务，请对比 Asg_RH 用例图，简述如何利用不同时代、不同地区产品的用例图，展现、突出创新业务和技术
  3. 如何利用用例图定位创新思路（业务创新、或技术创新、或商业模式创新）在系统中的作用
  4. 请使用 SCRUM 方法，选择一个用例图，编制某定旅馆开发的需求（backlog）开发计划表
  5. 根据任务4，参考 [使用用例点估算软件成本](https://www.ibm.com/developerworks/cn/rational/edge/09/mar09/collaris_dekker/index.html)，给出项目用例点的估算