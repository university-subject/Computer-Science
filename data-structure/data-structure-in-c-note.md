collect and note by JingShing

# Data Structure in C

## Dialog目錄

* [CHAPTER 1 BASIC CONCEPT](#CHAPTER-1-BASIC-CONCEPT)

## 資料結構

* 教學目標：

  資料結構主要是在研究如何把原始資料透過組織安排，存放到電腦中的一門學問，資料結構之目的亦在於如何有效撰寫程式。為了了解資料結構對於程式之影響，我們將使用C程式語言作為了解資料結構觀念之基本工具。因此，C語言程式之寫作基本觀念不可或缺。

* 教科書

  "Fundamentals of Data Structures in C", 2nd edition, by Horowitz et al.

## CHAPTER 1 BASIC CONCEPT

### Outline

* [**Overview : System Life Cycle(系統生命週期)**](#System-Life-Cycle)

* [Algorithm Specification(演算法定義)](#Algorithm-Specification)

* Data Abstraction(資料抽象化)

* Performance Analysis(效率分析)

* Performance Measurement(效率測量)

### System Life Cycle

* Requirements (需求）
  * 例如：定義專案目標、輸入是什麼、輸出是什麼
* Analysis (分析）: bottom-up vs. top-down
  * bottom-up: 比較沒有結構化與整體的計劃
  * top-down: 根據程式最後的目標，將程式分割成數個片段
* Design(設計) : data objects (物件) and operations (運算)
  * 例如：(物件) 學生、成績、教授；(運算) 新增課程、搜尋課程
* Refinement and coding(改良與編碼) 
* Verification(驗證) 
  * Correctness proofs (例如：數學証明)
  * Testing (例如：用switch指令測試每一種狀況)
  * Error removal (例如：利用前兩項與說明文件輔助除錯)

### Algorithm Specification

* Definition: An algorithm is a finite set of instructions that accomplishes a particular task.(有限個指令的集合,可完成一項特定工作)
* Criteria
  * Input(輸入): zero or more quantities
  * Output(輸出): at least one quantity is produced
  * Definiteness(明確的): each instruction is clear and unambiguous
  * Finiteness(有限的): terminate after a finite number of steps
  * `Effectiveness`(有效率的): instruction is basic enough to be carried out by a person using only pencil and paper

### Example 1.1

* Selection Sort (選擇排序法): sort a set of n unsorted integers.
* Solution: find the smallest and place it next in the sorted list
* However, the describe is not an algorithm, because it do not tell us
  * How the integers are initially stored
  * Where we should place the result

### Program 1.2: Selection sort algorithm

* Selection Sort (選擇排序法): sort a set of n unsorted integers.

* Assume: integers are stored in an array, list, such that the ith integer is stored in the ith position, list[i].

* Algorithm:

  ```c
  for( i = 0; i < n ; i++ ) {    
      Examine list [i] to list[n 1] and suppose that the    
      smallest integer is at list [min];     
      Interchange list[i] and list [min];
  }
  ```

  #### An example for selection sort

  <center>sample list

  | *i*  | [0]  | [1]  | [2]  | [3]  | [4]  | [5]  | [6]  | [7]  | [8]  |
  | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- |
  |      | 14   | 7    | 2    | 20   | 13   | 31   | 17   | 25   | 36   |
  | 0    | 2    | 7    | 14   | 20   | 13   | 31   | 17   | 25   | 36   |
  | 1    | 2    | 7    | 14   | 20   | 13   | 31   | 17   | 25   | 36   |
  | 2    | 2    | 7    | 13   | 20   | 14   | 31   | 17   | 25   | 36   |
  | 3    | 2    | 7    | 13   | 14   | 20   | 31   | 17   | 25   | 36   |
  | 4    | 2    | 7    | 13   | 14   | 17   | 31   | 20   | 25   | 36   |
  | 5    | 2    | 7    | 13   | 14   | 17   | 20   | 31   | 25   | 36   |
  | 6    | 2    | 7    | 13   | 14   | 17   | 20   | 25   | 31   | 36   |
  | 7    | 2    | 7    | 13   | 14   | 17   | 20   | 25   | 31   | 36   |
  | 8    | 2    | 7    | 13   | 14   | 17   | 20   | 25   | 31   | 36   |

>  22/9/15
