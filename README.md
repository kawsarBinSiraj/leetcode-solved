# leetcode-solved


## 791. Custom Sort String
You are given two strings order and s. All the characters of order are unique and were sorted in some custom order previously.

Permute the characters of s so that they match the order that order was sorted. More specifically, if a character x occurs before a character y in order, then x should occur before y in the permuted string.

Return any permutation of s that satisfies this property.

Example 2: <br/>
Input: order = "cbafg", s = "abcd" <br/>
Output: "cbad"


Solution : <br/>

<pre><code> 
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
<code/><pre/>
    
    
    
    
    
    
    
## 1539. Kth Missing Positive Number   
Given an array arr of positive integers sorted in a strictly increasing order, and an integer k.
Return the kth positive integer that is missing from this array.
 
Input: arr = [1,2,3,4], k = 2 <br/>
Output: 6 <br/>
Explanation: The missing positive integers are [5,6,7,...]. The 2nd missing positive integer is 6.
    
