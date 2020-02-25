### [数据结构 排序 - 插入排序](#top)  <b id="top"></b>
`插入排序（Insertion sort）是一种简单直观且稳定的排序算法。` 

------
- [x] [`1.直接插入排序`](#target1)

------

#####  [1.直接插入排序](#top) <b id="target1"></b> 
`如果有一个已经有序的数据序列，要求在这个已经排好的数据序列中插入一个数，但要求插入后此数据序列仍然有序，这个时候就要用到一种新的排序方法——插入排序法,算法适用于少量数据的排序，时间复杂度O(n^2)。`


```c
/*从小到大  不带哨兵 5 8 45 89 99 45 */
void InsertSort(int *a, int length){    
    for (int i = 1; i < length; i++)
    {
        if(a[i] < a[i - 1]){
            int pivot = a[i];
            int j;
            for(j = i - 1 ; a[j] > pivot  && j >= 0; j-- ){ 
                a[j + 1] = a[j];
            }
            a[j + 1] = pivot;
        }
    }
}
```

```c
/*从大到小 不带哨兵 */
void InsertSortReverse(int *a, int length){    
    for (int i = 1; i < length; i++)
    {
        if(a[i] > a[i - 1]){
            int pivot = a[i];
            int j;
            for(j = i - 1 ; a[j] < pivot  && j >= 0; j-- ){
                a[j + 1] = a[j];
            }
            a[j + 1] = pivot;
        }
    }
}
```

--------------------
`作者:` `蒋星 JxKicker` 
`完成时间`:`2020年2月25日18:25:35`
`备注信息`: `任意使用` 
