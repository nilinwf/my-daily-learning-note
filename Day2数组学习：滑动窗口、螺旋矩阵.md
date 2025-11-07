# 代码随想录算法训练营74期|Day2 数组Part02 滑动窗口、螺旋矩阵

| 题目     | Leetcode地址 |
| ----------- | ----------- |
|209.长度最小子数组      | [力扣题目链接](https://leetcode.cn/problems/minimum-size-subarray-sum/)      |
|904.水果成篮   | [力扣题目链接](https://leetcode.cn/problems/fruit-into-baskets/)        |
|59.螺旋矩阵II  |[力扣题目链接](https://leetcode.cn/problems/spiral-matrix-ii/description/)
|54. 螺旋矩阵 |[力扣题目链接](https://leetcode.cn/problems/spiral-matrix/description/)
|58. 区间和   |[力扣题目链接](https://kamacoder.com/problempage.php?pid=1070)|
|27.移除元素      | [力扣题目链接](https://leetcode.cn/problems/remove-element/description/)      |
| 26.删除排序数组中的重复项   | [力扣题目链接](https://leetcode.cn/problems/remove-duplicates-from-sorted-array/)        |
|283. 移动零|[力扣题目链接](https://leetcode.cn/problems/move-zeroes/)
|844. 比较含退格的字符串|[力扣题目链接](https://leetcode.cn/problems/backspace-string-compare/)
|977. 有序数组的平方|[力扣题目链接](https://leetcode.cn/problems/squares-of-a-sorted-array/)|

## 滑动窗口总结
1.暴力求解的时间复杂度为O(n^2)

2.滑动窗口时间复杂度O(n)，空间复杂度O(1)，就是不断的调节子序列的起始位置和终止位置。**初始化数组较大长度窗口，当满足窗口内数组和大于target时，再去缩小窗口起点**
  
  起始位置如何移动，如何移动起点位置？如何移动结束位置？
  
  1.j从0开始的，收集窗口下的sums和
  
  2.while**持续判断**sums是否大于等于target，确定当前窗口长度subL=j-i+1
  
  3.ans = min(resualt,subL)取当前值与最小长度
  
  4.sums -= nums[i], i+=1

变形下的滑动窗口：双指针动态调整窗口大小

 1 .水果成篮问题，创建哈希表（字典），记录品种个数，kind为限制。问题转化为：**求最长连续子数组，其中最多包含两种不同的元素**。right扩展窗口 当大于2时候，left收缩窗口， 每次循环都更新最大值。使用技巧       kindfound[fruits[right]] += 1  自动处理键不存在的情况；时间复杂度O(n)每个元素最多进窗口一次
 
 2. 最小覆盖子串**好难！！反复思考一下**

## 螺旋矩阵

 如59.螺旋矩阵II所示
   边界条件是左闭右开，容易错的点：分不清边界条件
   1. 上边：j在变，范围(starty, n-offset): nums[startx][j] = count
   2. 右边：i在变，范围(startx, n-offset): nums[i][n-offset] = count
   3. 下边：j在变，范围(n-offset, starty, -1): nums[n-offset][j] = count
   4. 左边：i在变，范围(n-offset, startx, -1): nums[i][starty] = count

如题54. 螺旋矩阵

3.技巧

① 前缀和的思想：重复利用计算过的子数组之和，降低区间查询需要累加计算的次数





  
