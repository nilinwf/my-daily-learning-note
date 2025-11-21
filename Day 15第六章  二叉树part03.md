# 代码随想录算法训练营74期| 第六章  二叉树 part03 



| 题目     | Leetcode地址 |
| ----------- | ----------- |
|110. 平衡二叉树 | [力扣题目链接](https://leetcode.cn/problems/balanced-binary-tree/)      |
|257. 二叉树的所有路径 （优先掌握递归） | [力扣题目链接](https://leetcode.cn/problems/binary-tree-paths/description/)      |
|404.左叶子之和 | [力扣题目链接](https://leetcode.cn/problems/sum-of-left-leaves/)      |
|222.完全二叉树的节点个数 | [力扣题目链接](https://leetcode.cn/problems/minimum-depth-of-binary-tree/description/)      |



### 平衡二叉树
求**深度**用前序遍历（中、左、右）

    -确定回溯函数的返回值（node）
    -终止条件：如果是左子树遍历的节点返回-1，则继续向上返回-1；同理右子树遍历的节点返回-1，继续向上返回-1；
    -判断内部循环：其他条件下的如果是左右子树的高度差大于1，那么也是返回-1；否则结果result等于1+max(leftHeight, rightHeight)

求**高度**用后序遍历（左、右、中）


### 二叉树的所有路径
使用前序遍历（中、左、右），后边的子序列信息传递给节点；

    -确定递归函数的参数与返回值：返回值node，路径path，返回值result数组
    -确定终止条件：做孩子为空 and 右孩子为空，此时将path转为字符串类型，每个字符之间放置“->”，sPath = '->'.join(map(str, path))，执行result.pushback(sPath)
    -单个循环内部情况：每遍历一遍要把节点加进来，按照中、前、后的遍历.

    但此题，需要把中序【收集节点】，因为终止条件为到叶子结点就结束，如果中序放在循环后边的话，路径中节点会没有加入path中，所以把path.push.back(cur.val)
放在循环之前。

    -如果左节点不为空，使用递归函数，再执行path.pop.back()
    -如果右节点不为空，使用递归函数，再执行path.pop.back()


### 左叶子之和
思想：需要父节点去判断该节点是不是左孩子，所以选择后序遍历（左、右、中），root根节点的左子树、右子树的sum和分开进行计算。

  -确定递归函数的参数和返回值
  
  -确定函数的终止条件：if node == None:return 0 or 遍历到叶子结点的时候也返回到0【可以写也可以不写，不写的情况下就递归再多一轮】
  
  -内部循环条件：左、右、中：
  
      -左：如果我们当前节点的左孩子不为空，且左孩子的左孩子为空【左孩子为叶子结点】，同时左孩子的右孩子也为空：此时即为左叶子结点，记录该~~~~比如图中的节点“9”
      -右：右子树的值=递归函数（node.right）
      -中：sum_val = leftsum+rightsum
  <img width="227" height="210" alt="QQ截图20251121160657" src="https://github.com/user-attachments/assets/f96e7103-2a87-4c01-a9a9-c1a9affd8f40" />


### 完全二叉树的节点个数--使用了**后序遍历**：满二叉树的特性：节点数=2ek-1个节点，如果判断子树[左、右子树]是否是满二叉树【是则+1即为深度】，如果是返回上一级【根节点】
思想：利用满二叉树的特性，判断左右子树的外侧深度是否相等，相等则计算2^k-1，
      -参数返回为node
      
      -终止条件：if node == None: return 0  ；子树是不是满二叉树
      
      -单层递归逻辑：
          -左：左子树的数量，向左去递归；
          -右：右子树的数量向右去递归；
          -中：result = leftsum+ rightsum

<img width="298" height="149" alt="QQ截图20251121170619" src="https://github.com/user-attachments/assets/6594f3b5-2c2b-473f-90e3-dfa351abcb39" />

满二叉树：一棵深度为k的二叉树，如果他有2^k-1个节点，则称为满二叉树，左图；

完全二叉树：除了最后一层外，其余所有层的节点数都达到最大，并且最后一层的所有节点都集中在最左边，右图；



<img width="772" height="278" alt="QQ截图20251121193625" src="https://github.com/user-attachments/assets/a127d597-c278-46a3-90c9-8f0121122f22" />







      
