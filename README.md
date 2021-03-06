# 说明
记录分布式系统学习过程中相关的关键知识点，如一致性协议，以及开源工具的使用。



引用知乎上[马超的总结](https://www.zhihu.com/question/23645117)：

```
分布式系统主要包含3个部分：
  1. 分布式存储系统 
  2. 分布式计算系统 
  3. 分布式管理系统
    
分布式存储大概分4个子方向：
  1. 结构化存储 
  2. 非结构化存储 
  3. 半结构化存储 
  4. In-memory 存储
   分布式存储系统有一系列的理论、算法、技术作为支撑：例如 Paxos, CAP, Consistent **Hash, Timing (时钟), 2PC, 3PC 等等。
那么如何掌握好这些技术呢？以我个人的经验，掌握这些内容一定要理解其对应的上下文。什么意思呢？就是一定要去思考为什么在当下环境
需要某项技术，如果没有这个技术用其它技术替代是否可行，而不是一味的陷入大量的细节之中。例如：如何掌握好 Paxos?  Paxos本质上
来说是一个三阶段提交，更 high level 讲是一个分布式锁。理解paxos必须一步一步从最简单的场景出发，比如从最简单的 master-backup 
出发，发现不行，衍生出多数派读写，发现还是不行，再到 paxos.  之后再了解其变种，比如 fast paxos, multi-paxos. 同理为什么
需要 Consistent Hash, 我们可以先思考如果用简单range partition 划分数据有什么问题。再比如学习 2pc, 3pc 这样的技术时，
可以想想他们和paxos 有什么关系，能否替代 paxos。
作者：马超链接：https://www.zhihu.com/question/23645117/answer/124708083来源：知乎著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。

```



开始我这边可能整理的不会太系统，会从一个问题点着手学习。







