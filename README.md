# sum-of-array-elements-by-recursion-in-C

#include<stdio.h>


int findsum(int arr[] , int start , int length );


int main(){
    int n,i,sum;
    int arr[100];
    printf("enter size of array=");
    scanf("%d",&n);
    printf("\nenter elements=");
    for(i=0;i<n;i++){
    scanf("%d",&arr[i]);   
    }
    sum=findsum(arr , 0, n);
    printf("sum=%d",sum);
    
    
    
    
    return 0;
}

int findsum(int arr[] , int start , int length ){
    if(start>=length){
        return 0;
        
    }
    else{
        return (arr[start] + findsum(arr,start+1,length));
    }
}
