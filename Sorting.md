# Sorting

<details>
<summary><h2> Bubble Sort </h2></summary>
  <details>
  <summary>Written Notes</summary>
  <br />
    <img src='https://user-images.githubusercontent.com/60965415/206712341-4dee407c-9200-458a-8951-f72a846092a6.png' height=1000>
<!--   ![image]() -->
  
  </details> 
  <details>
  <summary>Example</summary>

  <b>Array --> [5 , 4 , 1 , 3 , 2]</b>

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
 </details>
</details>
 
 
 <details>
<summary><h2> Selection Sort </h2></summary>

 <details>
<summary> Written Notes </summary>

  
  ![image](https://user-images.githubusercontent.com/60965415/206713458-97bade6e-33ef-4c6c-be84-d75251d35468.png)
  
</details> 
 <details>
<summary>Example</summary>

  <b>Array --> [5 , 4 , 1 , 3 , 2]</b>

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

</details>
 </details>



 <details>
<summary><h2> Insertion Sort </h2></summary>

 <details>
<summary> Written Notes </summary>

  ![image](https://user-images.githubusercontent.com/60965415/206715026-60ca630c-c9f0-4dfc-bae5-fe72d7c5ce3e.png)
  
</details> 
 <details>
<summary>Example</summary>

  <b>Array --> [5 , 4 , 1 , 3 , 2]</b>

**Code**


```java

   public static void insertionSort(int[] arr){
        for(int i=1;i<arr.length;i++){
            int cur=arr[i];
            int pre=i-1;
            while(pre>=0 && arr[pre]>cur){
                arr[pre+1]=arr[pre];
                pre--;
            }
            arr[pre+1]=cur;
        }
        System.out.print("Using Insertion Sort --> ");
        printArray(arr);
    }
 

 
```

</details>
 </details>



 <details>
<summary><h2> Counting Sort </h2></summary>

 <details>
<summary> Written Notes </summary>

  ![image](https://user-images.githubusercontent.com/60965415/206715388-ab870ebd-606a-4dbe-9476-9f7efbaf2499.png)
  
</details> 
 <details>
<summary>Example</summary>

  <b>Array --> [5 , 4 , 1 , 3 , 2]</b>

**Code**


```java

   public static void countingSort(int arr[]){
        int range=Integer.MIN_VALUE;
        for(int i=0;i<arr.length;i++){
            range=Math.max(range, arr[i]);
        }
        int[] countArr=new int[range+1];
        for(int i=0;i<arr.length;i++){
            countArr[arr[i]]++;
        }
        int j=0;
        for(int i=0;i<countArr.length;i++){
            while(countArr[i]>0){
                arr[j]=i;
                j++;
                countArr[i]--;
            }
        }
        System.out.print("Using Counting Sort --> ");
        printArray(arr);
    }


 
```

</details>
 </details>
