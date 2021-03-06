## it‘s like a markov chain?
动态规划很强的一个感觉就是状态机，能使用状态机转换的地方一定不会从bare question出发。这点逻辑思想和学习是一样的。markov讲当前状态只和上一个时刻的状态相关，与之前的无关。那DP问题就很像是一个multi branch markov问题？具体叫什么我也忘了。值得去查找一下。

那么到现在真正明白的为什么叫做动态规划：当前的新事件，可以继承到之前的任何一个状态，而不单单仅是上一个时刻的状态

就好像是个二维的array，要看新来一个，对于之前的每一个结果产生的影响，从而选取最优解。看起来有一点返自然规律：举个例子想起来瑞荣玩的游戏。可以开车倒退回之前的任何一个时刻。平行宇宙的感觉。真正讲：维护的一个array在每个时刻的数据都是当前最优解。相当于我们对于一个因果系统的问题，维护一个选择池。可以针对以前任意一个池选项来挑选更合适当前的方法。好像上升到哲学层面，人生也是一个选择池。本以为因为人生，或者时间是个单向轴回不去所以不好做这种选择池。选择池在于池的广泛和当前最优解。大概解释了人 多创造各种可能性，抓住每个机遇的逻辑吧。

## questions
1. 1，3，5凑11 简称为11点问题 
2. LIS longest increasing subsequence 哈哈现在看真的太典型啦
3. 二维吃苹果问题 两个方向来，构造状态矩阵的时候要从左往右 从上往下的构造以确保每个量都可以被reach out

## Basic coding ideas
这部分呢看到了一些个很常运用的coding手段。属于building block之类的吧😝
### min
traverse through an array. update while find a smaller one

### multiple layer
其实想这个东西很久了。有时候会绕在里边。在动态规划中设定了一个d(i) array. i这个index有两层作用。 一层作为原array的index另一层作为构造的d的index，而两者恰好对应。

## More training
1. [LIS O(nLogn)](https://www.felix021.com/blog/read.php?1587)
2. 无向图G有N个结点(1 < N <= 1000)及一些边，每一条边上带有正的权重值。 找到结点1到结点N的最短路径，或者输出不存在这样的路径。提示：在每一步中，对于那些没有计算过的结点， 及那些已经计算出从结点1到它的最短路径的结点，如果它们间有边， 则计算从结点1到未计算结点的最短路径。
3. [ZigZag - 2003 TCCC Semifinals 3](https://community.topcoder.com/tc?module=ProblemDetail&rd=4493&pm=1259)
4. [BadNeighbors - 2004 TCCC Round 4](https://community.topcoder.com/tc?module=ProblemDetail&rd=5009&pm=2402)
5. [FlowerGarden - 2004 TCCC Round 1](https://community.topcoder.com/tc?module=ProblemDetail&rd=5006&pm=1918)
6. [AvoidRoads - 2003 TCO Semifinals 4](https://community.topcoder.com/tc?module=ProblemDetail&rd=4709&pm=1889)
7. [ChessMetric - 2003 TCCC Round 4](https://community.topcoder.com/tc?module=ProblemDetail&rd=4482&pm=1592)
8. [DP must check out this](http://www.geeksforgeeks.org/dynamic-programming-set-3-longest-increasing-subsequence/)
