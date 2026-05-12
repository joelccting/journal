# 一張STL標準樣板函式庫

1. 容器(container)
   
   1. 循序式容器(sequence containers)：線性的資料儲存容器。分成三種
      
      1. vector
      
      2. deque
      
      3. list
   
   2. 關聯式容器(associative containers)：非線性儲存容器，可以快速搜尋資料，可以用於儲存資料的集合，與鍵值與儲存值(key 與 value)配對的資料結構，分成四種
      
      1. set
      
      2. multiset
      
      3. map
      
      4. multimap
   
   3. 配接器(container adapters)：序列式容器的變形，限制插入與取出資料是在序列式容器的第一個元素或最後一個元素。分成三種
      
      1. stack
      
      2. queue
      
      3. priority_queue

2. 迭代器(iterator)：類似指標，可以指定容器中個別的元素，可以與演算法功能
   一起使用。
   
   1. 只有 vector 與 deque 支援隨機的迭代器
   
   2. 循序式容器 list、關聯式容器 set、multiset、map 與 multimap 支援雙向的迭代器
   
   3. 配接器 stack、queue 與 priority_queue 不支援迭代器的使用

3. 演算法(algorithm)

# vector

- 迭代器  begin, end, 

- 新增或刪除元素 push_back, pop_back, insert, erase, clear

- 讀取元素 a[i], front, back

- 儲存空間 empty, size

# stack

# queue

# dictionary/map

# set

- properties:
  
  - unique elements, no duplicate allowed
  
  - sorted order, ascending by default
  
  - associative: elements are accessed by value, not by index
  
  - immutable values: can insert or erase elements, but values of existing elements can not be modified

- operations
  
  - insert
  
  - find
  
  - count
  
  - erase
  
  - size
  
  - empty
  
  - clear

### unordered_set

### multiset

## sequence/list

## priority queue

## graph

## tree
