## 第三周算法笔记

### 递归

#### 1. 递归 Recursion

> 循环，通过函数体来进行的循环

![image-20201018194132556](C:\Users\QY\AppData\Roaming\Typora\typora-user-images\image-20201018194132556.png)

---

* 递归终止条件
* 处理当前层逻辑
* 下探到下一层
* 清理当前层

 ![image-20201018194414623](C:\Users\QY\AppData\Roaming\Typora\typora-user-images\image-20201018194414623.png)

---

* 不要人肉递归
* 找最近重复子问题
* 数学归纳法

---

### 分治与回溯

![image-20201018212157507](C:\Users\Cris\AppData\Roaming\Typora\typora-user-images\image-20201018212157507.png)

* 终止条件
* 处理当前逻辑
* 下探到下一层

> 回溯法尝试分步解决一个问题，当其尝试发现现有的分步答案不能得到有效的正确的解答的时候，将取消上几步的计算，再通过其他可能的分步解答再次尝试寻找问题的答案