## Count Primes 

> https://leetcode.com/problems/count-primes/

```javascript
/**
 * @param {number} n
 * @return {number}
 */
var countPrimes = function(n) {
    var result = 0
    n--
    while(n > 1){if(isPrime(n--)){result++}}
    return result
};

var isPrime = function(n){
    if(n === 2){return true}
    var m = 2
    var limit = Math.sqrt(n)
    while(m <= limit){if(n % m++ === 0){return false}}
    return true
}
```