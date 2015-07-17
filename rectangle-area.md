## Rectangle Area 

> https://leetcode.com/problems/rectangle-area/

```javascript
/**
 * @param {number} A
 * @param {number} B
 * @param {number} C
 * @param {number} D
 * @param {number} E
 * @param {number} F
 * @param {number} G
 * @param {number} H
 * @return {number}
 */
var computeArea = function(A, B, C, D, E, F, G, H) {
    var x, y
    if(E < A){
        if(G < A){
            x = 0
        }else if(G < C){
            x = G - A
        }else{
            x = C - A
        }
    }else if(E < C){
        if(G < C){
            x = G - E
        }else{
            x = C - E
        }
    }else {
        x = 0
    }
    if(F < B){
        if(H < B){
            y = 0
        }else if(H < D){
            y = H - B
        }else{
            y = D - B
        }
    }else if(F < D){
        if(H < D){
            y = H - F
        }else{
            y = D - F
        }
    }else {
        y = 0
    }
    return (C - A) * (D - B) + (G - E) * (H - F) - x * y
};


```