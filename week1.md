- ##### 26. [删除有序数组中的重复项](https://leetcode-cn.com/problems/remove-duplicates-from-sorted-array/)

```javascript
/**
 *
 * @param {number[]} nums
 * @return {number}
 */

var removeDuplicates = function (nums) {
  if (nums === null || nums.length === 0) {
    return 0;
  }

  let len = 0,
    idx = 1;

  while (idx < nums.length) {
    if (nums[len] !== nums[idx]) {
      nums[len + 1] = nums[idx];

      len++;
    }

    idx++;
  }

  return len++;
};
```

- ##### 189. [旋转数组](https://leetcode-cn.com/problems/rotate-array/)

```javascript
/**
 * @param {number[]} nums
 * @param {number} k
 * @return {void} Do not return anything, modify nums in-place instead.
 */
let reverse = function (nums, start, end) {
  while (start < end) {
    [nums[start++], nums[end--]] = [nums[end], nums[start]];
  }
};
var rotate = function (nums, k) {
  k %= nums.length;

  reverse(nums, 0, nums.length - 1);
  reverse(nums, 0, k - 1);
  reverse(nums, k, nums.length - 1);

  return nums;
};
```

思路主要是：

1. 翻转 k 个元素，即 nums 中后 k 个元素会被翻转到数组前面
2.

- ##### 21. [合并两个有序链表](https://leetcode-cn.com/problems/merge-two-sorted-lists/)
