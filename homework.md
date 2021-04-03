1. ##### [70. 爬楼梯](https://leetcode-cn.com/problems/climbing-stairs/)

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

2. ##### [66. 加一](https://leetcode-cn.com/problems/plus-one/)

```javascript

```

3. ##### [1. 两数之和](https://leetcode-cn.com/problems/two-sum/)

```javascript

```

4. ##### [24. 两两交换链表中的节点](https://leetcode-cn.com/problems/swap-nodes-in-pairs/)

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
