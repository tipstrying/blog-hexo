---
title: 将数字变成 0 的操作次数
date: 2022-05-27 22:38:34
tags: 力扣题库
---

给你一个非负整数 num ，请你返回将它变成 0 所需要的步数。 如果当前数字是偶数，你需要把它除以 2 ；否则，减去 1 。

#### 示例
输入：num = 14
输出：6
解释：
步骤 1) 14 是偶数，除以 2 得到 7 。
步骤 2） 7 是奇数，减 1 得到 6 。
步骤 3） 6 是偶数，除以 2 得到 3 。
步骤 4） 3 是奇数，减 1 得到 2 。
步骤 5） 2 是偶数，除以 2 得到 1 。
步骤 6） 1 是奇数，减 1 得到 0 。

来源：力扣（LeetCode）
链接：https://leetcode.cn/problems/number-of-steps-to-reduce-a-number-to-zero
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。


### 方法一：

最容易想到的办法就是逐步判断上一步的结果，如果为奇数就减去 1，如果是偶数就除以 2，循环往复直至结果为零。
代码：
```
class Solution {
public:
    int numberOfSteps(int num) {
        int steps = 0;
        while(num > 0)
        {
            if(num % 2 > 0 )
            {
                num --;
            }else
            {
                num = num / 2;
            }
            steps++;
        }
        return steps;
    }
};
```


