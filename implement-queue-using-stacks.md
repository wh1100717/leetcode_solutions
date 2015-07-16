## Implement Queue using Stacks 

> https://leetcode.com/problems/implement-queue-using-stacks/

```javascript
/**
 * @constructor
 */
var Queue = function() {
    this.el = []
};

/**
 * @param {number} x
 * @returns {void}
 */
Queue.prototype.push = function(x) {
    this.el.push(x)
};

/**
 * @returns {void}
 */
Queue.prototype.pop = function() {
    this.el.splice(0, 1)
};

/**
 * @returns {number}
 */
Queue.prototype.peek = function() {
    return this.el.slice(0, 1)[0]
};

/**
 * @returns {boolean}
 */
Queue.prototype.empty = function() {
    return this.el.length === 0
};
```