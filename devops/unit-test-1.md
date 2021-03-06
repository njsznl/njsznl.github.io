# 背景
关于想做单元测试，有感于咱们的产品、项目提测质量差，测试时间经常被压缩，测试质量无法保证，导致团队常陷于无休止修改缺陷的泥潭，灵感来源于今年的Tid大会，关于精准测试概念的分享，今天分享的内容就是引进精准思想进行单元测试。

# 什么是单元测试

## 传统定义
在计算机编程中，单元测试（英文：Unit Testing）又称模块测试，是针对程序模块来进行正确性验证的测试工作。程序单元是应用的最小可测部件。在过程化编程中，一个单元就是单个程序、函数、过程等。在面向对象编程，最小单元就是方法、包括基类（超类）、派生类（子类）中的方法。

## 定义新解
以上定义在任何一本单元测试相关书本里，或者百度百科里，都可以搜到，但是随着单元测试的发展和业界人士的实践，单元测试已经不限于传统的定义，对于单元测试的“单元”有了变化，或者说了有了进一步的认识和新的解释。

### 关于对单元测试的单元的理解：
一个单元从某种程度上代表系统中的一个“功能单元”，或者一个完整“用例”。例如：从调用系统的一个公共方法，到产生一个测试可见的最终结果，期间这个系统发生的行为总和为一个工作单元。例如：我们通过系统的公共API就可以观察到某个方法的一个可见的最终结果，而无需查看系统的内部状态。
我们或许可以这么定义单元测试：一个单元测试是一段测试代码，这段测试代码调用一个工作单元，并验证该工作单元的最终结果，如果这个最终结果和预期不一致，单元测试就失败了。一个单元测试的范围可以小到一个方法，也可以大到多个类。

### 单元和集成测试的区别：
我们发现单元测试扩展后，好像和我们的集成测试概念有了冲突，那么我们把集成测试和单元测试的重新进行一下归类和区分，或许我们可以这样进行区分：任何测试，如果它运行速度不快，结果不稳定，或者要用到被测试单元的一个或这个多个真实依赖，我们就可以简单的把它认为是集成测试。例如：一个测试要使用真实的系统时间，或者要读取真实的文件系统，或者要连接一个真实的数据库，那么这个测试我们可以简单的认为他在做集成测试。例如：一个测试不能控制系统时间，在代码中使用了系统当前时间，那么每次测试执行使用的都是不同的时间，每次测试本质上结果都是不同的，那么这个测试是不稳定的。

## 总之，
单元测试和集成测试本身都不是坏事，占有同等重要的地位，但两种测试要分开进行，不同的阶段要进行不同的测试，明确测试当前所处的阶段，清楚当前测试的目标是什么，即无论什么测试都要有很强的目的性和针对性，切忌漫无目的瞎测。（软件测试阶段：单元测试、集成测试、系统测试、验收测试。）

