# Sorting

##  Bubble Sort <h2> **T(n) --> O(n)** </h2>

**Written Notes**

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


##  Selection Sort

**Written Notes**

![image](https://user-images.githubusercontent.com/60965415/206713458-97bade6e-33ef-4c6c-be84-d75251d35468.png)


**Example** 

### Array --> [5 , 4 , 1 , 3 , 2]

**Code**


```java

public static void selectionSort(int[] arr){
        for(int i=0;i<arr.length-1;i++){
            int minPos=i;
            for(int j=i+1;j<arr.length;j++){
                if(arr[minPos]>arr[j]){
                    minPos=j;
                }
                
            }
            // System.out.println("minPos "+minPos);
            if(minPos!=i){
                    int temp=arr[minPos];
                    arr[minPos]=arr[i];
                    arr[i]=temp;
                }
        }
        System.out.print("Using Selection Sort --> ");
        printArray(arr);
    }

 
```

