//# array1
//shif negative number in one side and positive other sidein array
//(-5 ,-2  , 10 , -8 , 9 , 10)

#include<iostream>
using namespace std;


int main(){
    
    int arr[6] = {-5 , -2 , 10 , -8 , 9 , -3};
    
    
    for(int i = 0; i < 6; i++){
        cout<<arr[i]<<"   ";
    }
    cout<<endl;
    
    for(int i = 0; i < 6; i++){
        if(i == 0){
            if(arr[i] > 0){
                i = 1;
                while(arr[i] < 0){
                    
                     if(arr[i] < 0){
                        int temp = arr[i];
                        arr[i] = arr[i - 1];
                        arr[i - 1] = temp;
                    }
                      i++;
                      
                }
            }
            
            else{
                continue;
            }
        }
        
        if(arr[i] < 0){
            continue;
        }
        else{
            int j = i + 1;
            if(arr[j] < 0){
                int temp = arr[j];
                arr[j] = arr[i];
                arr[i] = temp;
            }
            /*
            else{
            while(arr[j] > 0){
                 
            }
            }
            */
        }
        
        
    }
    
    for(int i = 0; i < 6; i++){
        cout<<arr[i]<<"  "<<endl;
    }
 }
