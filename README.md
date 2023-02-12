# SEARCH-INSERT-POSITION-C-

**Intuition**
Brute Force

**Approach**
-* initialise low=0; mid;
-* high upto nums.size()-1
-* when low is less then high mid=low+(high-low)/2
-* if nums[mid]==target tehn return mid
-* if nums[mid]<target low=mid+1 else high =mid-1;
_8 return low;

**Complexity**
****Time complexity:****
o(nlogn)

Space complexity:
o(n)

**Code**
class Solution {
public:

    int searchInsert(vector<int>& nums, int target) 
   {
    int lo=0;
     int hi=nums.size()-1;
    int mid;
    while(lo<=hi)
    {
    mid=lo+(hi-lo)/2;
    if(nums[mid]==target)
        return mid;
    else if(nums[mid]<target)
        lo=mid+1;
    else
        hi=mid-1;
        }
    return lo;
   }

   };
