# 代码随想录算法训练营74期| 第六章  二叉树 part02 



| 题目     | Leetcode地址 |
| ----------- | ----------- |
|226.翻转二叉树  | [力扣题目链接](https://leetcode.cn/problems/invert-binary-tree/description/)      |
|101. 对称二叉树 | [力扣题目链接](https://leetcode.cn/problems/symmetric-tree/description/)      |
|104.二叉树的最大深度 | [力扣题目链接](https://leetcode.cn/problems/maximum-depth-of-binary-tree/description/)      |
|111.二叉树的最小深度 | [力扣题目链接](https://leetcode.cn/problems/minimum-depth-of-binary-tree/description/)      |



### 翻转二叉树
可以使用前序遍历与后序遍历中进行reverse()操作
    -使用递归
    -使用迭代

### 对称二叉树：思路判断是否可以翻转，判断根节点的左子树、右子树是否相等

    -只能使用**后序遍历**，只能把底部孩子的信息向上一层传递信息，

### 二叉树的最大深度
深度：二叉树任一个节点到根节点。。**前序遍历**

高度：二叉树中任意一个节点到叶子结点的距离。。**后序遍历**

根节点的最大高度==该二叉树的最大深度

### 二叉树的最小深度
最小深度是从根节点到最近叶子节点的最短路径上的节点数量。

使用后序遍历【左右中】将子节点的情况返回给上一级父节点
