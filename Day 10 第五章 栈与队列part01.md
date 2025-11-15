# 代码随想录算法训练营74期| 第五章 栈与队列part01  


| 题目     | Leetcode地址 |
| ----------- | ----------- |
|232.用栈实现队列 | [力扣题目链接](https://leetcode.cn/problems/implement-queue-using-stacks/description/)      |
|225.用队列实现栈 | [力扣题目链接](https://leetcode.cn/problems/implement-stack-using-queues/description/)      |
|20.有效的括号 | [力扣题目链接](https://leetcode.cn/problems/valid-parentheses/description/)      |
|1047.删除字符串中的所有相邻重复项 | [力扣题目链接](https://leetcode.cn/problems/remove-all-adjacent-duplicates-in-string/description/)      |


用栈实现队列：用两个栈，一个栈记录入栈，另一个栈作为出栈；入栈正常放入即可，出栈需要改变顺序，先把入栈的所有元素都放在出栈


用队列实现栈：

    -push直接使用队列的push即可

    -移除并返回栈顶元素：用一个队列的思路，将size-1个元素按照顺序取出来之后又放回队列中去，将第size个取出即为pop操作
    
    -top获取第一个栈中的第一个元素

有效的括号:使用栈模拟三种不匹配的情况

      -情况一：当我们顺序遍历时候，遇到"("时候把")"放入栈中，同理其他的，接下来遇到对应的括号之后进行弹出消除，如果最后栈不为空，则说明不匹配::

      -情况二：也是遍历栈顶元素，和我们当前遍历的有方向的括号类型不匹配

      -情况二：遍历字符串的时候发现，当遍历到有括号的时候，栈为空


删除字符串中的所有相邻重复项：利用栈的特性，创建一个空栈，然后

    -情况1.stack为空，就加入字符
    
    -情况2.如果stack[-1]栈的最后一个元素 == 当前char,则pop出，否则就加入当前stack中
