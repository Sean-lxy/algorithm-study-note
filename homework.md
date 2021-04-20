- ### `简单` [70. 爬楼梯](https://leetcode-cn.com/problems/climbing-stairs/)

```javascript

var climbStairs = function(n) {
    // 数组实现, 空间占用较高
    const arr = [0, 1, 2];

    for (let i = 3; i <= n; i++>) {
        arr[i] = arr[i -1] + arr[i - 2];
    }

    return arr[n];

    // 双指针实现
    if(n < 3) {
        return n;
    }

    let x = 1, y = 2, z;

    for (let i = 3; i <= n; i++) {
        z = x + y;
        x = y;
        y = z;
    }

    return z;
}

```

- ### [66. 加一](https://leetcode-cn.com/problems/plus-one/)

```javascript

```

- ### [1. 两数之和](https://leetcode-cn.com/problems/two-sum/)

```javascript

```

- ### [24. 两两交换链表中的节点](https://leetcode-cn.com/problems/swap-nodes-in-pairs/)

```javascript
var swapPairs = function (head) {
  // 递归实现
  if (head === null || head.next === null) {
    return head;
  }

  // 存储目标节点的next节点
  const temp = head.next;

  // 递归调用，将head.next指向下一个目标的next节点
  head.next = swapPairs(temp.next);
  temp.next = head;

  return temp;

  // 循环实现
};
```

- ### [21. 合并两个有序链表](https://leetcode-cn.com/problems/merge-two-sorted-lists/)

- ### [299. 猜数字游戏](https://leetcode-cn.com/problems/bulls-and-cows/)

- ### [641. 设计循环双端队列](https://leetcode-cn.com/problems/design-circular-deque/)

- ### [350. 两个数组的交集 II](https://leetcode-cn.com/problems/intersection-of-two-arrays-ii/)

- ### [](https://leetcode-cn.com/problems/hua-dong-chuang-kou-de-zui-da-zhi-lcof/)

- ### [剑指 Offer 59 - I. 滑动窗口的最大值](https://leetcode-cn.com/problems/remove-outermost-parentheses/)

- ### [412. Fizz Buzz](https://leetcode-cn.com/problems/fizz-buzz/)

- ### [258. 各位相加](https://leetcode-cn.com/problems/add-digits/)

- ### [104. 二叉树的最大深度](https://leetcode-cn.com/problems/maximum-depth-of-binary-tree/)

- ### [51. N 皇后](https://leetcode-cn.com/problems/n-queens/)

- ### [94. 二叉树的中序遍历](https://leetcode-cn.com/problems/binary-tree-inorder-traversal/)

- ### [剑指 Offer 05. 替换空格](https://leetcode-cn.com/problems/ti-huan-kong-ge-lcof/)

- ### [剑指 Offer 06. 从尾到头打印链表](https://leetcode-cn.com/problems/cong-wei-dao-tou-da-yin-lian-biao-lcof/)

- ### [剑指 Offer 68 - II. 二叉树的最近公共祖先](https://leetcode-cn.com/problems/er-cha-shu-de-zui-jin-gong-gong-zu-xian-lcof/)

- ### [17. 电话号码的字母组合](https://leetcode-cn.com/problems/letter-combinations-of-a-phone-number/)

- ### [77. 组合](https://leetcode-cn.com/problems/combinations/)

- ### [面试题 17.09. 第 k 个数](https://leetcode-cn.com/problems/get-kth-magic-number-lcci/)
