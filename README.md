# LeetCodeInJava
#Algorithm
##List
1.Two Sum




#Detail

Given an array of integers, return indices of the two numbers such that they add up to a specific target.
You may assume that each input would have exactly one solution.

#Example:
Given nums = [2, 7, 11, 15], target = 9,
Because nums[0] + nums[1] = 2 + 7 = 9,
return [0, 1].

[LeetCode link](https://leetcode.com/problems/two-sum/)
###my solution:
*O(n^2)的写法：*

```java
package leetcode;
/** 
@author  wangjx 
@date 创建时间：2016年10月25日 下午8:39:03 
@version 1.0 
@parameter 
@return 
*/
public class Solution {
    public static int[] twoSum(int[] nums, int target) {
	        int[] a = new int[2];
		for(int i = 0;i<nums.length;i++){
	            int start = nums[i];
	            for(int j= i+1;j<nums.length;j++){
	            	int end = nums[j];
	            	if(start+end==target){
	            		a[0] = i;
	            		a[1] = j;
	            	}
	            }
	        }
		return a;
	    }
}
```


*O(n)写法：*
```java
public class Solution {
    public static int[] twoSum(int[] nums, int target) {
	    int[] result = new int[2];
        Map<Integer, Integer> map = new HashMap<Integer, Integer>();
        for (int i = 0; i < nums.length; i++) {
            if (map.containsKey(target - nums[i])) {
                result[1] = i ;
                result[0] = map.get(target - nums[i]);
                return result;
            }
            map.put(nums[i], i);
        }
        return result;
}
}
```

2.Longest Substring
#desc:
  Given a string, find the length of the longest substring without repeating characters.
Examples:
Given "abcabcbb", the answer is "abc", which the length is 3.
Given "bbbbb", the answer is "b", with the length of 1.
Given "pwwkew", the answer is "wke", with the length of 3. Note that the answer must be a substring, "pwke" is a subsequence and not a substring.
