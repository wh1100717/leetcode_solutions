## Implement Stack using Queues

> https://leetcode.com/problems/implement-stack-using-queues/

```javascript
/**
 * @constructor
 */
var Stack = function() {
    this.el = []
};

/**
 * @param {number} x
 * @returns {void}
 */
Stack.prototype.push = function(x) {
    this.el.splice(0, 0, x)
};

/**
 * @returns {void}
 */
Stack.prototype.pop = function() {
    this.el.splice(0, 1)
};

/**
 * @returns {number}
 */
Stack.prototype.top = function() {
    return this.el.slice(0, 1)[0]
};

/**
 * @returns {boolean}
 */
Stack.prototype.empty = function() {
    return this.el.length === 0
};
```