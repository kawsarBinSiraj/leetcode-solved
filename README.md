# leetcode-solved

### <a href="https://leetcode.com/problems/custom-sort-string/" target="_blank"> 791. Custom Sort String<a/>
Here is my solution : 
```
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
                                      
### <a href="https://leetcode.com/problems/custom-sort-string/" target="_blank"> 1539. Kth Missing Positive Number<a/>
    
Here is my solution : 
```
var findKthPositive = function(arr, k) {
    let store = [];
    for (let i = 1;; i++) {
        if (!arr.includes(i)) store.push(i)
        if (store.length === k) break
    }
    return store[k - 1]
};
 ```
