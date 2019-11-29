
#include <stdio.h>\
#include <stdlib.h>

void insertionSort(int arr[], int size){
    
    //iterative variables
    int i, j, k;
    
    for(i = 1; i < size; i++){
        
        k = arr[i];
        j = i - 1;
        
        //while loop
        while(j >= 0 && arr[j] > k){
            arr[j + 1] = arr[j];
            j = j - 1;
        }
        
        arr[j + 1] = k;
        
    }
    
}


void displaySort(int arr[], int s){
    
    for(int i = 0; i < s; i++){
        printf("%d ", arr[i]);
    }
}

int main()
{
    
    int arr[] = { 12, 8, 44, 38, 59, 33, 45, 74, 9 };
    int s = sizeof(arr) / sizeof(arr[0]);
    
    insertionSort(arr, s);
    
    
    displaySort(arr, s);
    
    
    return 0;
}
