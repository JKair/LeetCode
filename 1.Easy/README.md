- Easy:

1. Excel Sheet Column Number：
这道题主要是思路的转换，一开始做的时候没转换过来，其实把这道题当成进制转换来做就可以了

1. Implement strStr()：
这道题可以很简单一行就解决，也可以做得有深度点，本来使用kmp，看到鸟哥的微博知道sunday或者bm更高效更容易理解，于是学习了sunday，当做练手了

1. pow(x,n):
快速幂AC

1. Remove Element:
总觉得这道题并不严谨，没有判定多个值一样的问题，处理是很简单的。直接删除然后返回长度

1. Plus One:
一开始没看懂在讲什么，后来才明白，给定一个数组然后+1，比如[1,9] + 1 = [2,0]，注意类型转换就可以了

1. Same Tree：
遍历结构而已，很简单，递归思想！

1. Symmetric Tree ：
这道题也很简单，算是Same Tree的变形，只要拆分成两棵树，两棵树镜像对称，那就只要一棵树的左等于另一棵树的右就可以解决问题了。依然是递归解决

1. Binary Tree Level Order Traversal：
其实就是分深度而已，使用一个参数去控制，搞定。依旧是递归解决

1. Maximum Depth of Binary Tree：
其实就是一个打擂和遍历而已。

1. Minimum Depth of Binary Tree：
这个和max不大一样，但是总体处理起来还是差不多的。解题过程中有点陷入思维误区，因为要的是最小深度，把left和right赋值为0了，之后永远是0。后来把right和left的值赋值为int_max之后才解决。思路也是递归算而已，算左子树的最小深度，再算右子树的深度，然后每次往下走就深度+1，最后得出左子树和右子树谁小就可以了。有点像分治。

1. Path Sum ：
这道题就是计算有没有路径的值等于sum而已，其实就是遍历，只要一边遍历一遍把根节点的值加上上一个节点的值就可以了，注意一个点，要算的是到叶子节点的地方，不是找一条路径等于就好！

1. Remove Duplicates from Sorted List：
删除前后一样的节点，很简单。只要判断前后节点一样，那么就让当前节点等于下一个节点，相当于缩短链表。

1. Binary Tree Level Order Traversal II:
这道题很简单了，就是遍历记录而已，可以参考[Maximum Depth of Binary Tree](https://github.com/JKair/LeetCodeSolution/blob/master/1.Easy/Maximum%20Depth%20of%20Binary%20Tree.cpp) 也是类似解法，变形

1. Remove Nth Node From End of List：
这道题只是去除节点而已，倒过来数，不知道是不是我英文不好，坑爹的题目，说n的值永远有效，我一直以为n是在链表的深度范围内，结果简直坑爹，不是那样子的，注意这个细节就好了，其他不难

1. Valid Parentheses：
验证是不是符合括号对称而已，用栈的思想就可以解决了。

1. Merge Two Sorted Lists：
生成一个新的链表而已，很简单的链表操作。C++ 20ms

1. Climbing Stairs ：
这道题就是普通的爬楼梯题目，具体这样理解，如果我有一阶楼梯，那么只有一种情况，如果两阶，那么有两种，如果三阶，那么就分解一下，其实我们可以理解为爬n-1阶楼梯最后再爬一阶或者爬n-2阶楼梯再爬两阶，也就是说，n-1阶楼梯还有n-2阶楼梯的爬法的总和，因为我们一次可以爬一阶或者两阶！也于是我们可以得出一条公式就是S[n-1]+S[n-2] && S[0]=1 && S[1]=2。解题有两种思想，一种是迭代，一种是递归，递归很简介，三行代码就写完了，但是超时严重，于是我改用了迭代，AC了。