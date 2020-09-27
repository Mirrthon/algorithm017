### 两数之和

```
class Solution {
    public int[] twoSum(int[] nums, int target) {
        HashMap<Integer, Integer> map = new HashMap<>();
        int[] result = new int[2];
        for(int i = 0; i < nums.length; i++){
            if(map.containsKey(nums[i])){
                result[0] = i;
                result[1] = map.get(nums[i]);
                return result;
            }
            map.put(target-nums[i],i);
        }
        return null;
    }
}
```

### 合并两个有序链表

```
class Solution {
    public ListNode mergeTwoLists(ListNode l1, ListNode l2) {
        if (l1 == null) return l2;
        if (l2 == null) return l1;
        //第一个链表 第二个链表 已经合并好的来链表
        //若第一个大于第二个，则第二个的下一个就是第一个和第二个的下一个的merge
        if(l1.val > l2.val){
            l2.next = mergeTwoLists(l1, l2.next);
            return l2;
        }else{
            l1.next = mergeTwoLists(l1.next, l2);
            return l1;
        }
       
    }
}
```

### 加一

```
class Solution {
    public int[] plusOne(int[] digits) {
        for(int i = digits.length - 1; i >= 0; i--){
            if (digits[i] != 9){
                digits[i]++;
                return digits;
            }
            digits[i] = 0;
        }
        int[] digit = new int[digits.length + 1];
        digit[0] = 1;
        return digit;
    }
}
```

