# LeetCodeInJava
Algorithm
#List
1.Two Sum




#Detail

Given an array of integers, return indices of the two numbers such that they add up to a specific target.
You may assume that each input would have exactly one solution.

Example:
Given nums = [2, 7, 11, 15], target = 9,
Because nums[0] + nums[1] = 2 + 7 = 9,
return [0, 1].

LeetCode link:
https://leetcode.com/problems/two-sum/
-my solution:

package leetcode;
/** 
@author  wangjx 
@date 创建时间：2016年10月25日 下午8:39:03 
@version 1.0 
@parameter 
@return 
*/
public class TwoSum {
    public static int[] twoSum(int[] nums, int target) {
	    	
	        for(int i = 0;i<nums.length;i++){
	            int start = nums[i];
	            for(int j= 0;j<nums.length-i;j++){
	            	int end = nums[j];
	            	if(start+end==target){
	            		int[] a = {i,j};
	            		return a;
	            	}
	            }
	        }
			return null;
	    }
	public static void main(String[] args) {
		int[] nums = {8,2,7,9};
		int[] x =twoSum(nums, 9);
		System.out.println(x[0]+"   "+x[1]);
	}
}



