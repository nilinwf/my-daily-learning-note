| 题目     | Leetcode地址 |
| ----------- | ----------- |
|203.移除链表元素      | [力扣题目链接](https://leetcode.cn/problems/remove-linked-list-elements/)      |
|707.设计链表   | [力扣题目链接](https://leetcode.cn/problems/design-linked-list/)        |
|206.反转链表   |[力扣题目链接](https://leetcode.cn/problems/reverse-linked-list/description/)     |

## 链表

# 链表类型：非连续存储
1.单链表：通过指针串联在一起的线性结构，每一个节点有数据域与指针域（存放下一个节点的指针），最后节点的指针指向null为空

2.双链表：每一个节点有两个指针域，一个指向下一个节点一个指向上一个节点，既可以向前查询也可以向后查询

3.循环链表：链表首尾相连，可以用来解决约瑟夫环问题
~~~
class ListNode:
  def __init__(self, val, next=None):
      self.val = val
      self.next = next
~~~
# 203.移除链表元素
  1.构造虚拟头结点:dummy_head = ListNode(next = head)
  2.设计链表：
    1.获取下表为index的节点：判断方位，用循环构造指针寻找下标
    2.插入头结点：需要构造new_node，把new_node指向dummy_head.next（因为dummy_head.next指向head头结点），然后再把dummy_head.next指向new_node与此同时，修改self.size+=1
    3.插入尾部节点:构造循环以找到尾部节点，当尾部curr.next为空时，找到尾结点，在尾结点加上新节点，并更新self.size += 1
    4.在索引位置加入：同上循环找到index节点
    5.在索引位置删除：同上循环找到index节点
  3.翻转链表：
    1.双指针解法：需要三个指针，注意顺序，
    2.递归解法：太难了暂时还不是很理解

  
