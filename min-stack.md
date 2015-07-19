## Min Stack 

> https://leetcode.com/problems/min-stack/

```javascript
/**
 * @constructor
 */
var MinStack = function() {
    this.stack = []
    this.min = []
};

/**
 * @param {number} x
 * @returns {void}
 */
MinStack.prototype.push = function(x) {
    this.stack.push(x)
    if(this.min.length === 0 || x <= this.min[this.min.length -1]){
        this.min.push(x)
    }
};

/**
 * @returns {void}
 */
MinStack.prototype.pop = function() {
    var p = this.stack.pop()
    if(this.min[this.min.length - 1] === p){
        this.min.pop()
    }
};

/**
 * @returns {number}
 */
MinStack.prototype.top = function() {
    return this.stack[this.stack.length - 1]
};

/**
 * @returns {number}
 */
MinStack.prototype.getMin = function() {
    return this.min[this.min.length - 1]

};
```