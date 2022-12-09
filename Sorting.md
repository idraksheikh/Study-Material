# Sorting

##  Bubble Sort

![image](https://user-images.githubusercontent.com/60965415/206712341-4dee407c-9200-458a-8951-f72a846092a6.png)

**Example** 

### Array --> [5 , 4 , 1 , 3 , 2]

**Code**


```java

 public static void bubbleSort(int[] arr){
        for(int i=0;i<arr.length-1;i++){
            int swap=0;
            for(int j=0;j<arr.length-1-i;j++){
                if(arr[j]>arr[j+1]){
                    int temp=arr[j];
                    arr[j]=arr[j+1];
                    arr[j+1]=temp;
                    swap++;
                }
                if(swap==0)break;
            }
        }
        System.out.print("Using Bubble Sort --> ");
        printArray(arr);
    }

```
