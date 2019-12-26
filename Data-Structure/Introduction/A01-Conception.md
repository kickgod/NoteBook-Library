### [第一章数据结构--绪论](#top) <b id="top"></b>
:one: `数据结构是计算机存储、组织数据的方式。`  
:two: `数据结构是指相互之间存在一种或多种特定关系的数据元素的集合。主要包含三个方面的内容：1.逻辑结构
2.存储结构 3.数据的运算`


------
- [x] [`1.基本概念`](#target1)
- [x] [`2.数据结构三要素`](#target2)
------


##### [1.基本命令](#top) <b id="target1"></b>
----
**`数据`**:`信息的载, 是描述客观事物属性的数，字符和所有能输入到计算机中并被计算机程序识别和处理的符号的集合`  
**`数据元素`**:`数据元素是数据的基本单位, 一个数据元素可以有若干个数据线组成,数据项是构成数据元素不可分割的最小单位`  
**`数据项`**:`是构成数据元素不可分割的最小单位`  

|`学号`|`姓名`|`年级`|`学院`|`专业`|
|:---|:--|:---|:---|:---|
|`2016990938`|`Smith tnome`|`2016级`|`计算机科学学院`|`计算机科学与技术`|
|`2016990939`|`Willian Hazzlt`|`2016级`|`计算机科学学院`|`计算机科学与技术`|

`如上一行就是一个数据元素, 而姓名，年级等就是一个数据项`

**`数据类型`**:`具有相同性质的数据元素的集合,是数据的一个子集`
* 1.`原子类型`: `不可再分的数据类型` `int 类型`
* 2.`结构类型`: `其值可以再分解为若干个成分的数据类型` `struct student { int age, char * name, int number}`
* 3.`抽象数据类型`:`抽象数据组织及其与之相关的操作` 
    ```c#
     public class Racer:IComparable<Racer>
     {
         public int  Id{get;}
         public string FirstNmae{get;set;}
         public string LastName{get;set;}
         public string Country{get;set;}
         public int Wins{get;set;}

         public string GetName=> $"{this.FirstNmae} {this.LastName}";

         public override string ToString(){
             return $"{this.Id} Name:{this.FirstNmae} {this.LastName} Country:{Country} Wins Time:{Wins}";
         }

         public  int CompareTo(Racer obj)
         {
             return this.Id.CompareTo(obj.Id);
         }

         public Racer(int id,string fname,string lname,string cou,int win){
             this.Id=id;
             this.FirstNmae=fname;
             this.LastName=lname;
             this.Country=cou;
             this.Wins=win;
         }
     }
    ```
