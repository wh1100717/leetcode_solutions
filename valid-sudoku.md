## Valid Sudoku 

> https://leetcode.com/problems/valid-sudoku/

```javascript
/**
 * @param {character[][]} board
 * @return {boolean}
 */
var isValidSudoku = function(board) {
    for(var i = 0; i < 9; i++){
        var m = {},
            n = {}
        for(var j = 0; j < 9; j++){
            if(board[i][j] !== "."){
                if(m[board[i][j]]){
                    return false
                }else{
                    m[board[i][j]] = true
                }
            }
        }
        for(var j = 0; j < 9; j++){
            if(board[j][i] !== "."){
                if(n[board[j][i]]){
                    return false
                }else{
                    n[board[j][i]] = true
                }
            }
        }
    }
    for(var i = 0; i < 9; i = i + 3){
        for(var j = 0; j < 9; j = j + 3){
            var k = {}
            if(board[i][j] !== "."){k[board[i][j]] = true}
            if(k[board[i][j+1]]){return false}
            if(board[i][j+1] !== "."){k[board[i][j+1]] = true}

            if(k[board[i][j+2]]){return false}
            if(board[i][j+2] !== "."){k[board[i][j+2]] = true}
            if(k[board[i+1][j]]){return false}
            if(board[i+1][j] !== "."){k[board[i+1][j]] = true}
            if(k[board[i+1][j+1]]){return false}
            if(board[i+1][j+1] !== "."){k[board[i+1][j+1]] = true}
            if(k[board[i+1][j+2]]){return false}
            if(board[i+1][j+2] !== "."){k[board[i+1][j+2]] = true}
            if(k[board[i+2][j]]){return false}
            if(board[i+2][j] !== "."){k[board[i+2][j]] = true}
            if(k[board[i+2][j+1]]){return false}
            if(board[i+2][j+1] !== "."){k[board[i+2][j+1]] = true}
            if(k[board[i+2][j+2]]){return false}
            if(board[i+2][j+2] !== "."){k[board[i+2][j+2]] = true}
        }
    }
    return true
};
```