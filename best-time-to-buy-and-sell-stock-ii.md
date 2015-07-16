## Best Time to Buy and Sell Stock II 

> https://leetcode.com/problems/best-time-to-buy-and-sell-stock-ii/

```javascript
/**
 * @param {number[]} prices
 * @return {number}
 */
var maxProfit = function(prices) {
    t = 0
    for(var index=0; index < prices.length - 1; index++){
        if(prices[index + 1] > prices[index]){
            t += prices[index + 1] - prices[index]
        }
    }
    return t
};
```