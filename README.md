    #include<bits/stdc++.h>
    using namespace std;


    class Solution {
    public:
           int secondLargestElement(vector<int>& nums){
            //your code goes here
            int largest = nums[0];
            int slargest = -1;
            for(int i = 0;i< nums.size();i++){
            if(nums[i]>largest){
            slargest = largest;
            largest = nums[i];
    }
    else if( nums[i] < largest  && nums[i] > slargest){
        slargest = nums[i];
    }
    }
        return slargest;
    }
    };

    int main(){
    Solution s ;

    vector<int> nums= {8,8,7,6,5};

    
    int ans = s.secondLargestElement(nums);
    cout<<" the second largest element is "<<ans;
    }
