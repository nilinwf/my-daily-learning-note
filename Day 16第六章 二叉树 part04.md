# 代码随想录算法训练营74期| 第六章  二叉树 part04 



| 题目     | Leetcode地址 |
| ----------- | ----------- |
|513.找树左下角的值 | [力扣题目链接](https://leetcode.cn/problems/find-bottom-left-tree-value/description/)      |
|112.路径总和  | [力扣题目链接](https://leetcode.cn/problems/path-sum/description/)      |
|113.路径总和 II | [力扣题目链接](https://leetcode.cn/problems/sum-of-left-leaves/)      |
|106.从中序与后序遍历序列构造二叉树 | (https://leetcode.cn/problems/construct-binary-tree-from-inorder-and-postorder-traversal/description/) | [力扣题目链接](https://leetcode.cn/problems/construct-binary-tree-from-inorder-and-postorder-traversal/description/)      |
|105.从前序与中序遍历序列构造二叉树 | (https://leetcode.cn/problems/construct-binary-tree-from-inorder-and-postorder-traversal/description/) | [力扣题目链接](https://leetcode.cn/problems/construct-binary-tree-from-inorder-and-postorder-traversal/description/)      |



### 找树左下角的值
思路：优先遍历左侧，找深度最大的最左边的节点即可

回溯方法：

    -确定回溯函数参数和返回值（root, depth）
    
    -终止条件：遍历到叶子结点：左右孩子为空条件下，比较当前节点深度跟maxdepth
    
    -单层递归逻辑：向左去递归遍历，深度++，递归调用向左子树，深度--【回溯】；同理右边也是

迭代法：使用层序遍历本体使用层序遍历比较简单快捷

### 112.路径总和
迭代法：
    -此题自己写的时候，发现逻辑混乱，还有一个点即：忘记回溯，还有就是内部终止条件的return 到回溯函数的其他为止的时候，注意传递的逻辑，【因为原来以为只要有一个return True or False 即可，但后来发现他在回溯循环内部结束之后，也需要接收回溯结果进行判断True or False】


### 106.从中序与后序遍历序   越来越难了，有点吃不消了
思路：利用后序遍历知道根节点，然后在中序遍历中根据根节点划分前部分为左子树，后部分为右子树；循环往复根据后序遍历接下来的值。

分步骤为：

1.后序数组为0，空间节点

2.后序数组最后一个元素为节点元素

3.寻找中序数组位置作为切割垫

4.切中序数组

5.切后序数组

6.递归处理左区间、右区间
<img width="985" height="568" alt="QQ截图20251123200237" src="https://github.com/user-attachments/assets/70d1fde2-e6e7-4de3-b4c1-d8999b44e450" />

      
