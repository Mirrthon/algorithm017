## 第二周算法题目记录

### 1. 有效的字母异位词

> 字母出现的次数一样，但是顺序不一样
>
> 例如：anagram 与 nagaram 

---

> **步骤：**
>
> * **先沟通一遍**
> * **找最优解，即时间和空间复杂度都是最好的**
> *  **写代码**
> * **测试样例阐述**

```java
class Solution {
    public boolean isAnagram(String s, String t) {
        //如果长度不同则肯定不是字母异位词
        if(s.length() != t.length()) return false;
        
        //定义一个计数器
        int[] count = new int[26];

        //对于s中的每一个字母，可以根据字母位置为下标来进行计数
        for(int i = 0; i < s.length(); i++){
            count[s.charAt(i) - 'a']++;
            count[t.charAt(i) - 'a']--;
        }

        //遍历完以后检查每一个位置是否为0
        for(int j : count){
            if(j != 0) return false;
        }
        return true;
    }
}
```

### 2. 二叉树的前序遍历

```java
class Solution {
    public List<Integer> preorderTraversal(TreeNode root) {
        List<Integer> res = new ArrayList<>();
        preorder(root, res);
        return res;
    }
   
    private void preorder(TreeNode root, List<Integer> res){
        if(root != null){
            res.add(root.val);
            preorder(root.left, res);
            preorder(root.right, res);
        }
    }
}
```

