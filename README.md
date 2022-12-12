# SINGLE-NUMBER -
//single number III
class Solution {
    public int[] singleNumber(int[] nums) {
        int xor=0;
        for(int n:nums) xor^=n;
        int a=0;
        int diff= (xor )& (-xor);
        for(int n:nums)if((n & diff)==diff) a^=n;
        int res[]=new int[2];
        res[0]=a;
        res[1]=xor^a;
        return res;
        
    }
}-
