# 
#include<iostream>

using namespace std;

    int max_sum_non_adjacent(int arr[], int index){

            if(index==0) return arr[index]; 

            if(index<1) return 0;


            int pick = arr[index] + max_sum_non_adjacent(arr, index-2);

            int non_pick = 0+ max_sum_non_adjacent(arr, index-1 ); 


            return  max(pick, non_pick); 
    }
int main(){

    int arr[6] = {1,2,3,4,5,8}; 

    int n=5; 

  cout<<max_sum_non_adjacent(arr, n ); 
return 0;
}
