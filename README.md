# Live-and-learn

//Swift
  learning basic knowledge of Swift
  http://www.runoob.com/swift/swift-operators.html
  A html which is useable for swift newcomer
  
  
//Blog
  http://draveness.me/author/draveness/page/2/  高级工程师必看的源码解析
  
  
//OC-Style-Guide
  https://github.com/raywenderlich/objective-c-style-guide
  
  
//Separation of mechanism and policy
  https://en.wikipedia.org/wiki/Separation_of_mechanism_and_policy
  
  
//Separation of concern
https://en.wikipedia.org/wiki/Separation_of_concerns


//Onece and Only Once

  The principle of "once and only once" originated in the world of programming, where it is considered foolish to do something twice that only needs to be done once. As it applies to a wiki, it means that you shouldn't duplicate any information or keep multiple copies of documents organized in different ways.

  The violation of this principle can lead to many problems. These complications could include (but are certainly not limited to):

  One of the versions will soon be out of date, since it can be very difficult to remember to update them all. Worse, some wiki editors may not even be aware that the copies exist, and therefore won't realize that they need to edit the copy if they have edited the original.
  We will have more to overcome when we want to change the format of or reason for the documents' existence.
  Responsibilities in our community become scattered, leading to documents that are difficult to understand.
  It becomes immediately clear than none of these outcomes would be good for our wiki or our wiki community, therefore, we feel that the "once and only once" principle should be adhered to as closely as possible. This means that an individual   object or being should have only one page pertaining to it. Users should check for a page's existence before creating a   new one.


//SOLID（OO）原则
  在学习和使用OO设计的时候，我们应该明白：OO的出现使得软件工程师们能够用更接近真实世界的方法描述软件系统。然而，软件毕竟是建立在抽象层次上的东西，再怎么接近真实，也不能替代真实或被真实替代。 
  OO设计的五大原则之间并不是相互孤立的。彼此间存在着一定关联，一个可以是另一个原则的加强或是基础。违反其中的某一个，可能同时违反了其余的原则。因此应该把这些原则融会贯通，牢记在心！ 
  OO的五大原则是指SRP、OCP、LSP、DIP、ISP。 
  1. SRP（Single Responsibility Principle 单一职责原则） 
  单一职责很容易理解，也很容易实现。所谓单一职责，就是一个设计元素只做一件事。什么是“只做一件事”？简单说就是少管闲事。现实中就是如此，如果要你专心做一件事情，任何人都有信心可以做得很出色。 
  OCP作为OO的高层原则，主张使用“抽象(Abstraction)”和“多态(Polymorphism)”将设计中的静态结构改为动态结构，维持设计的封闭性。 
  2. OCP :开闭原则，很简单，一句话：“Closed for Modification; Open for   Extension”——“对变更关闭；对扩展开放”。开闭原则其实没什么好讲的，我将其归结为一个高层次的设计总则。OCP的动机很简单：软件是变化的。不论是优质的设计还是低劣的设计都无法回避这一问题。OCP说明了软件设计应该尽可能地使架构稳定而又容易满足不同的需求。   为什么要OCP？答案也很简单——重用。 
  3.LSP——里氏替换原则 
  OCP作为OO的高层原则，主张使用“抽象(Abstraction)”和“多态(Polymorphism)”将设计中的静态结构改为动态结构，维持设计的封闭性“抽象”是语言提供的功能。“多态”由继承语义实现。 如此，问题产生了：“我们如何去度量继承关系的质量？” 
  Liskov于1987年提出了一个关于继承的原则“Inheritance should ensure that any property proved about supertype objects also   holds for subtype objects.”——“继承必须确保超类所拥有的性质在子类中仍然成立。”也就是说，当一个子类的实例应该能够替换任何其超类的实例时，它们之间才具有is-A关系。 
  该原则称为Liskov Substitution Principle——里氏替换原则。 
  我们来研究一下LSP的实质。学习OO的时候，我们知道，一个对象是一组状态和一系列行为的组合体。状态是对象的内在特性，行为是对象的外在特性。LSP所表述的就是在同一个继承体系中的对象应该有共同的行为特征。 
  这一点上，表明了OO的继承与日常生活中的继承的本质区别。举一个例子：生物学的分类体系中把企鹅归属为鸟类。我们模仿这个体系，设计出这样的类和关系。 
  
  
  类“鸟”中有个方法fly，企鹅自然也继承了这个方法，可是企鹅不能飞阿，于是，我们在企鹅的类中覆盖了fly方法，告诉方法的调用者：企鹅是不会飞的。这完全符合常理。但是，这违反了LSP，企鹅是鸟的子类，可是企鹅却不能飞！需要注意的是，此处的“鸟”已经不再是生物学中的鸟了，它是软件中的一个类、一个抽象。 
  有人会说，企鹅不能飞很正常啊，而且这样编写代码也能正常编译，只要在使用这个类的客户代码中加一句判断就行了。但是，这就是问题 所在！首先，客户代码和“企鹅”的代码很有可能不是同时设计的，在当今软件外包一层又一层的开发模式下，你甚至根本不知道两个模块的原产地是哪里，也就谈不上去修改客户代码了。客户程序很可能是遗留系统的一部分，很可能已经不再维护，如果因为设计出这么一 个“企鹅  ”而导致必须修改客户代码，谁应该承担这部分责任呢？（大概是上帝吧，谁叫他让“企鹅”不能飞的。^_^）“修改客户代码”直接违反了OCP,这就是OCP的重要性。违反LSP将使既有的设计不能封闭！ 
  
  修正后的设计如下： 
  
  LSP并没有提供解决这个问题的方案，而只是提出了这么一个问题。 于是，工程师们开始关注如何确保对象的行为。1988年，B.   Meyer提出了Design by Contract（契约式设计）理论。DbC从形式化方法中借鉴了一套确保对象行为和自身状态的方法，其基本概念很简 单 ： 
  
      每个方法调用之前，该方法应该校验传入参数的正确性，只有正确才能执行该方法，否则认为调用方违反契约，不予执行。这称为前置条件(  Pre-condition)。 
      一旦通过前置条件的校验，方法必须执行，并且必须确保执行结果符合契约，这称之为后置条件(Post-condition)。 
      对象本身有一套对自身状态进行校验的检查条件，以确保该对象的本质不发生改变，这称之为不变式(Invariant)。 
      以上是单个对象的约束条件。为了满足LSP，当存在继承关系时，子类中方法的前置条件必须与超类中被覆盖的方法的前置条件相同或者更宽松；而子类中方法的后置条件必须与超类中被覆盖的方法的后置条件相同或者更为严格。 
  
  4.DIP 依赖倒置原则 
  依赖倒置（Dependence Inversion Principle）原则讲的是：要依赖于抽象，不要依赖于具体。 
  简单的说，依赖倒置原则要求客户端依赖于抽象耦合。原则表述： 
  抽象不应当依赖于细节；细节应当依赖于抽象； 
  要针对接口编程，不针对实现编程。 
  
  5.ISP 接口隔离原则 
  使用多个专门的接口比使用单一的总接口要好。广义的接口：一个接口相当于剧本中的一种角色，而此角色在一个舞台上由哪一个演员来演  则相当于接口的实现。因此一个接口应当简单的代表一个角色，而不是一个角色。，如果系统设计多哥角色的话，则应当每一个角色都由一  个特定的接口代表。狭义的接口（Interface）:接口隔离原则讲的就是同一个角色提供宽、窄不同的接口，以对付不同的客户端。
//技术债务
1、什么是“技术债务”？
  它就是“那些内在的事物，现在你不去解决，遗留下来（不干完），它就会阻碍未来开发”[Ward Cunningham]。   表面上，应用程序看起来质量很高且状况良好，但是这些问题却隐藏在下面。   QA（质量保证部门）甚至可能告诉你说，这个应用程序真是不错，几乎找不到缺陷，但是其中仍然存在“技术债务”，如果我们没有很好地管理并设法降低这些“技术债务”，那么，程序编写和维护的代价最终将会超过它对客户的价值。
  
  技术债务就像信用卡一样，会有很高的利息率，就如同给团队留下了大量的帐务开销。这种情况下，开销将会体现在时间花费和解决问题所需的努力上面。开发团队拖延债务的时间越长，所积累的利息就越多（会额外增加很多工作），付出的成本也就越高。
  
  另外，这还增加了实际的财务支出：开发团队处理技术债务所花费的时间，可以用在对团队有价值的其它工作上。同时，这些难读的代码引起的技术债务也让我们难以找到软件的缺陷。再且，理解代码所损失的时间还可以用来做其它更有价值的事情呢。

2、我们为何要累积技术债务呢？
  项目编码初期，不整理代码，不写单元测试，也不做测试驱动开发，整个团队粗制滥造出更多的“故事场景”。 这些问题通常都不会马上暴露出来，而循规蹈矩地编写代码往往需要更多的时间，特别是在早期阶段。

3、技术债务来自哪里？
  一、没有经验的开发人员 
      有些项目里面，编写Java/C#/Ruby的开发人员没有接受过培训，或者没有面向对象的观念。结果呢，他们会一直编写适用于他们曾经习惯的编程语言——像Visual Basic等——的代码。
  二、项目工期的压力 
      那些来自于经理或客户的显性压力和其它一些潜在的压力。“我们承诺在以后迭代（发布）的故事场景中做到这些”。开发团队会发现他们不会交付这些承诺的发行 版本（迭代版本），而是采取便捷的手段。“我们不得不把事情做完；我们无法承担修整代码所耗费的时间。如果这不是新特性/缺陷，那么就不用去做”。 不幸的是，这些观点还会得到管理人员的支持，特别是在管理层没有意识到这些成本的时候。
  三、凌乱而难读的代码。
      当一个方法或类中存在一些难读的代码，下一个开发人员继续这些工作的时候，就觉得他也没有必要迫使自己编写清晰的代码。所以，每次有人接手这些代码的时候，一小段脏乱的代码将会变成一大堆乱七八糟的代码。
  四、专业领域的代码
      往往有这样的观念：这些代码看起来就是很差劲，但是这不属于我的领域，所以我不能或不会改变它们。另外，对于修改专业领域的代码，开发人员也会觉得力不从心。
  五、过度复杂 
      开发人员经常趋向于在需求之前设计解决方案。而且，很多情况下他们的代码没有找到正确的方向，还会写一些没有用处的代码。或者，这些代码没有真正地符合需求，因为代码在问题还没有完全明白的时候就已经写完了。还有另外一种情况，过度设计花费了额外的时间，产生的代码不是不能使用就是不符合项目的需求。
  六、糟糕的设计
      有些解决方案只是设计不佳。但在设计不好的代码上面继续扩展，而不去解决这个问题，会使问题更加恶化。
      解决问题，这个问题的并不是一下子可以解决的，解决方案需要通过几个迭代周期。并且，你需要耐心，并要从多个角度寻找解决途径。

4、解决方案中的要点

    让开发人员接受语言方面的基本培训并教授他们面向对象的原理，从而把他们的理解力提升至入门阶段。要想既成功又有效的话，这需要花几个礼拜的时间培训，还需要有精通这方面的人员来跟进和支持这一系列培训。
    告诉开发人员和管理人员，当前的这些问题都是需要花费企业资金的。这点尤其重要，因为它会使解决这些问题的意义更加明确。你要清楚地告诉他们，管理人员会重视这些问题，并且已经开始着手偿还这些技术债务了。不断支持这些工作使之成为常规的原则之一，这样整个团队就会信任这个准则。
    提供一些培训，包括代码的坏味道，重构，单元测试和测试驱动开发等。还可以结合课堂会议，基于网络的材料和书籍来进行培训。
    在工作的时候，给他们一些空余时间去研究和练习他们的技能（一个礼拜两个小时应该是达成这个目标的最小的时间量）。练习的代码应该被丢弃，这样，他们就能无拘无束地尝试和试验一些事情，不管怎么样，他们不用在基础代码库上面进行练习。花点时间练习和研究应该是最有用的建议了。假如没有为他们提供空闲的时间，就压根不会发现真正合理的敏捷开发方式。这种组织方式也被称为“道场”-Dojo（更加详细的资料可以参考TDD Randori Session 和 TDD Randori Workshop）。
    使用工具（静态分析，单元测试，持续集成，自动化可接受性测试）来帮助团队发现、减少和衡量他们的技术债务量。应该在团队层面利用这些度量数据，而不能分享给管理人员。团队成员需要知道，他们并不会因为对这些技术债务的度量而接受奖励或者遭受惩罚。如果我们把这些度量数据报告给管理层，并由管理层来追踪的话，开发人员很快会找到一些窍门来规避它们，这样就失去了本来应有的价值了。
    当人们完成了他们的培训或者在技术上取得了少许提升时，应该得到奖励。奖励可以是给予一次认可的表彰或者是一些小小的礼物，但不要直接给予现金奖励。
    每两个礼拜进行一次午餐聚会和一些关于技术方面的学习型会议。利用这些会议来促进开发成员之间的讨论。提供午餐可以提高参会人数。另外比较重要的是需要管理人员每次都来出席，这样就很清楚的表明他们也一直支持大家提高技术。
    维护关于技术债务的备忘录 – 任何时候，如果开发人员发现一些无法立即应付的技术债务时，就需要填写一份技术债务登记卡。开发人员应该优先考虑这些技术债务，并花费10-15%的精力来偿还这些技术债务。大多数项目中，任何的一些小事都会使问题变得更加严重。
    基于这样的立场，你会发现问题，也会拥有机会。你的问题是：项目的基础代码一直在积累技术债务，但是这些债务已经开始下降了。然而，现在跟客户申请用于处理这些问题的资金会跟处理这些问题一样困难。你的机遇是：提高了开发人员的技能；清楚地表达了管理层对这项工作的支持，还有，软件的代码质量会不断改善，软件缺陷的数目也会不断减少。同时这也会很好的提高团队的整体开发能力。
