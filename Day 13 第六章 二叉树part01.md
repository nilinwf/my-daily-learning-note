# 代码随想录算法训练营74期| 第六章 二叉树part01  二叉树理论基础，二叉树的种类、二叉树的存储方式、二叉树节点定义、二叉树的遍历顺序


| 题目     | Leetcode地址 |
| ----------- | ----------- |
|144.前序遍历 | [力扣题目链接](https://leetcode.cn/problems/binary-tree-preorder-traversal/)      |
|145.后序遍历 | [力扣题目链接](https://leetcode.cn/problems/binary-tree-postorder-traversal/description/)      |
|94.中序遍历 | [力扣题目链接](https://leetcode.cn/problems/binary-tree-inorder-traversal/description/)      |
|102.二叉树的层序遍历|[力扣题目链接](https://leetcode.cn/problems/binary-tree-level-order-traversal/description/)      |
|107.二叉树的层序遍历II | [力扣题目链接](https://leetcode.cn/problems/binary-tree-level-order-traversal-ii/description/)      |
|199.二叉树的右视图| [力扣题目链接](https://leetcode.cn/problems/binary-tree-right-side-view/description/)      |
|637.二叉树的层平均值|[力扣题目链接](https://leetcode.cn/problems/average-of-levels-in-binary-tree/description/)      |
|429.N叉树的层序遍历 | [力扣题目链接](https://leetcode.cn/problems/binary-tree-inorder-traversal/description/)      |
|515.在每个树行中找最大值|[力扣题目链接](https://leetcode.cn/problems/find-largest-value-in-each-tree-row/description/)      |
|116.填充每个节点的下一个右侧节点指针| [力扣题目链接](https://leetcode.cn/problems/populating-next-right-pointers-in-each-node/description/)      |
| 题目     | Leetcode地址 |
| ----------- | ----------- |
/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
|117.填充每个节点的下一个右侧节点指针II| [力扣题目链接](https://leetcode.cn/problems/binary-tree-right-side-view/description/)      |
|104.二叉树的最大深度|[力扣题目链接](https://leetcode.cn/problems/n-ary-tree-level-order-traversal/description/)      |
|111.二叉树的最小深度|[力扣题目链接](https://leetcode.cn/problems/n-ary-tree-level-order-traversal/description/)      |
## 二叉树的种类
1.满二叉树，节点数量2ek-1
2.完全二叉树：底部的节点一定是从左往右是连续的
3.二叉搜索树（对节点只要满足顺序即可，对于节点的个数没有要求）：节点有顺序大小，左子数的所有节点都小于根节点（中间节点），右子数的所有节点都大于根节点，且左右子树都满足该条件
4.平衡二叉树：左子树与右子树的高度的绝对值差不能超过一


## 二叉树的存储方式
1.链式存储：
2.线性存储：

## 二叉树的遍历
1.深度优先搜索（前、中、后）：递归，栈的方式实现；非递归的方式：迭代法实现
    
      -前序遍历：中、左、右
      -中序遍历：左、中、右
      -后序遍历：左、右、中
  
2.广度优先搜索：**层序遍历**，使用队列【先进先出】


      
## 二叉树的定义
用链表方式实现，二叉树的定义；

代码实现中：

递归需要考虑的三个点：
    -确定递归函数的参数和返回值
    -确定终止条件
    -确定单层递归的逻辑

用队列实现层序遍历：借用一个辅助数据结构即队列来实现，队列先进先出，符合一层一层遍历的逻辑，而用栈先进后出适合模拟深度优先遍历也就是递归的逻辑。

而这种层序遍历方式就是图论中的广度优先遍历，只不过应用在二叉树上。
    
