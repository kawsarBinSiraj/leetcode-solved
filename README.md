# leetcode-solved

## [<a href="https://leetcode.com/problems/custom-sort-string/" target="_blank"> 791. Custom Sort String<a/>](https://leetcode.com/problems/custom-sort-string/)
```
/**
 * @param {string} order
 * @param {string} s
 * @return {string}
 */
var customSortString = function(order, s) {
    let c = s.split('').reduce((acc, item)=> {
        if (!order.includes(item)) acc += item;
        return  acc
    }, '')
    let a = order.split('').reduce((acc, item)=> {
            if (s.includes(item)) {
                let l = s.split(item).length
                for (let i = 1; i < l; i++) acc += item
            }
            return  acc
    }, '')
    return  a + c
}; 
 ```
                                      
