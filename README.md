## leetcode-solved ( https://leetcode.com/kawsarBinSiraj )

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


### <a href="https://leetcode.com/problems/detect-capital/" target="_blank"> 520. Detect Capital <a/>
    
Here is my solution : 
```
var detectCapitalUse = function(word) {
    return word.toLowerCase() === word || word.toUpperCase() === word || word.substring(1).toLowerCase() == word.substring(1)
};
 ```
    
    
### <a href="https://leetcode.com/problems/remove-duplicates-from-sorted-array/" target="_blank"> 26. Remove Duplicates from Sorted Array <a/>
    
Here is my solution : 
```
var removeDuplicates = function(nums) {
   let insertIndex = 1;
    for(let i = 1; i < nums.length; i++){
        // We skip to next index if we see a duplicate element
        if(nums[i - 1] != nums[i]){  
            /* Storing the unique element at insertIndex index and incrementing
               the insertIndex by 1 */
            nums[insertIndex] = nums[i];  
            insertIndex++; 
        }
    }
    return insertIndex;
};
 ```

                                
                                   
### <a href="https://leetcode.com/problems/palindrome-number/" target="_blank"> 9. Palindrome Number <a/>
    
Here is my solution : 
```
var isPalindrome = function(x) {
     if (x < 0 || (x % 10 === 0 && x !== 0)) {
        return false;
      }
    
    const reverse = (num) => {
      let rev = 0;
      while (num != 0) {
        rev = rev * 10 + num % 10;
        num = parseInt(num / 10, 10);
      }
      return rev;
    };
    
    return x === reverse(x);
};
 ```

    
    
 ### <a href="https://leetcode.com/problems/determine-if-string-halves-are-alike/description/" target="_blank"> 1704. Determine if String Halves Are Alike <a/>
    
Here is my solution : 
```
var halvesAreAlike = function(s) {
    let dl = s.length / 2;
    let a = s.substring(0, dl);
    let b = s.substring(dl);
    let c = (str)=> {
        let count = 0;
        for (let letter of str.toLowerCase()) {
            if (["a", "e", "i", "o", "u"].includes(letter)) count++
        }
        return count 
    }
   let ab = c(a);
   let bb = c(b);
   return ab === bb
};
 ```   
 
     
     
### <a href="https://leetcode.com/problems/two-sum/description/" target="_blank"> 1. Two Sum <a/>
    
Here is my solution : 
```
var twoSum = function(nums, target) {
    let firstIndex, secondIndex;
		let found = false;
		for (let i = 0; i < nums.length; i++) {
			for (let j = i + 1; j < nums.length; j++) {
				if (nums[i] + nums[j] === target) {
					firstIndex = i;
					secondIndex = j;
					found = true;
					break;
				}
			}
			if (found) break;
		}
		return [firstIndex, secondIndex];
};
 ```       
    
    
