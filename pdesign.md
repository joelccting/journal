# 程式設計分類題庫

1. 按照中正大學資工系一年級王銘宏老師114學年度程式設計課程進度分類
2. 代碼詳見 [GITHUB](https://github.com/joelccting/qbank.git)

## 2026/05/19 講義 CH18 Graph

## 2026/05/12 講義 CH17 Tree

## 2026/04/28 講義 CH16 Sorting

1. ZeroJudge a104. 排序：可以練習使用stdlib.h/qsort，也可以用自幹的排序

## 2026/04/14 講義 CH15 Stack and Queue

1. ZeroJudge b923. stack 堆疊的模板題
   基本題

2. ZeroJudge a017. 五則運算
   Horowitz的書有寫

3. UVa 12207. That's Your Queue
   $P=10^9$ 達Giga等級，不能真的開下去。UVa的C只支援ANSI，C99的語法不能用。

4. ZeroJudge b304. (或 UVa 673) - Parentheses Balance
   
   1. 注意保護stack的指標top：如果不保護，會在左中小括弧出現太多的時候壞掉
   
   2. 注意兩個條件的先後順序
      
      ```c
      if (top > -1 && stack[top] == '(')`
      ```
   
   3. 處理含有空白的一行輸入
      
      ```c
      if (fgets(s, LEN - 1, stdin) != NULL)
      {
       s[strcspn(s, "\r\n")] = 0;
       len = strlen(s);
      }
      ```
   
   4. 處理含有return的輸入
      
      ```c
      scanf("%*[\r\n]"); //銘宏老師講義的寫法
      while (getchar() != '\n'); //Gemini建議的寫法
      ```

5. ZeroJudge a229. 括號匹配問題
   看似是先排列再檢查是否合法(即暴力法)，但backtracking可以直接解決。

6. ZeroJudge c123 / UVa 514 - Rails
   不符合 $1,2,3,...,n$ 順序的測資，要先push起來，再pop出來驗證。小心題目會重複測試，所以該歸零的要歸零。
   
   ## 2026/03/31 實習課

7. Jinshi

---

1. Brute force.
   
   ## 2026/03/31 小考

2. Score

3. Coloring

4. NIN again

5. Arena

---

1. Sorting
2. x
3. x
4. Divide and conquer

## 2026/03/31 講義 CH14 Linked List

1. ZeroJudge b586. 文章壓縮 

## 2026/03/24 實習課

1. Marshalling Yard
2. **Escape from Tamon’s World**

---

The first one can be solved by linked list with array. 
延伸練習：

1. ZeroJudge b938. kevin 愛殺殺2. 

## 2026/03/17 實習課

1. Permutation
   Horowitz p.15-16 Program 1.9 給了一個排列的演算法，但它只能不重複，不能按字典序。問題在想要保持字典序，需要每次遞迴都要保持字典序。所以要改成向右移，再 backtrack 向左移。
   
   ```c
   #define SWAP(x,y,t) ((t)=(x),(x)=(y),(y)=(t))
   ```

2. Fibonacci Bit

---

Both can be solved by recursion.
延伸練習：

1. ZeroJudge a024. 最大公因數(GCD)
2. ZeroJudge a042. 平面圓形切割
3. ZeroJudge a044. 空間切割
4. ZeroJudge a227. 三龍杯 -> 河內之塔

## 2026/03/10 小考

1. NIN
2. Echo Cleaner
3. Alphabet Elimination Game
4. Help Xi

---

延伸練習：

1. ZeroJudge a020. 身分證檢驗
2. ZeroJudge a054. 電話客服中心

## 2026/03/03 講義 CH11 Recursion and backtracking

__Backtracking__ 透過 trial and error 來找答案

- 舉例：走迷宮來到岔路口，先選一條路走走看，如果發現前面是死路，就退回到上一個路口，改走另一條路。通常採用遞迴來實現。

- 可拆為三個動作：做選擇（Choose）： 在當前步驟選擇一個可能的選項。探索（Explore）： 進入下一層遞迴，繼續嘗試下一個位置。撤銷選擇（Backtrack）： 如果發現這條路走不通（不符合題目限制），就將剛才做的選擇撤銷，回到上一步狀態，改試其他選項。

- 在Cormen的書中，將backtracking歸類在DFS當中，未獨立章節書寫。

- 回溯法本質上是窮舉，和單純的暴力破解相比，相異之處在於、先產生所有可能的組合，最後才檢查哪一個是對的；回溯法則在過程中即做選擇。
  
  ```c
  void backtrack(路徑, 選擇列表) {
    if (滿足結束條件) {
        儲存結果;
        return;
    }
  
    for (選擇 : 選擇列表) {
        if (如果不符合約束條件) continue; // 剪枝
  
        做選擇;
        backtrack(路徑, 選擇列表); // 進入下一層
        撤銷選擇; // 這就是「回溯」的核心：回到執行前的狀態
    }
  }
  ```
1. ZeroJudge b689 棕櫚迷宮
2. ZeroJudge a229. 括號匹配問題
3. ZeroJudge c139. UVa 291 - The House Of Santa Claus
   看書，完全不知道如何下手，查AI才知。圖不大，用adjacent matrix即可；recursive

## Divide and Conquer

## Greedy Algorithm

## Brute Force

1. ZeroJudge a121. 質數又來囉

## Searching

## 質數

## TODO

1. ZeroJudge f698. 後序運算式求值
2. ZeroJudge e155. 10935 - Throwing cards away I
3. ZeroJudge e183. 10940 - Throwing cards away II
4. ZeroJudge c104. 00167 - The Sultan's Successors
5. ZeroJudge f606. 2. 流量
6. ZeroJudge g275. 1. 七言對聯
7. ZeroJudge c295. APCS-2016-1029-2最大和

## 數論

不知道理論、是解不出這類題目的。

## 上學期

1. ZeroJudge a244. 新手訓練 ~ for + if
   資料大小問題。兩個int相乘，仍以int的變數存放。以下是解方之一
   
   ```c
   int b, c;
   long long r = b;
   r *= c;
   ```

2. ZeroJudge a240. 第一題：$1/17$ 小數第 n 位 
   Start with a $remainder$ of $1$. Multiply the $remainder$ by $10$. The digit is $(remainder * 10) / 17$. The new $remainder$ is $(remainder * 10) \mod 17$. Repeat this $n$ times.

## 參考資料

1. 林盈達. 大學程式能力檢定: CPE祕笈. 二版. 臺北市: 美商麥格羅希爾國際股份有限公司臺灣分公司, 2021. Print.
2. Horowitz, Ellis, Sartaj Sahni, and Susan Anderson-Freed. Fundamentals of Data Structures in C. 2nd ed. Summit, NJ: Silicon Press, 2008. Print.
3. 黃建庭. C++程式設計解題入門. 初版. 臺北市: 松崗資產管理, 2016. Print. [黃建庭的教學網站](https://sites.google.com/view/zsgititit/)
4. 黃建庭. 圖解資料結構 : 使用C++. 初版. 新北市: 台科大圖書, 2022. Print.
5. 林奈爾, Reuven M Lerner, and 施威銘研究室. Python刷題鍛鍊班: 老手都刷過的50道程式題,求職面試最給力. 初版. 臺北市: 旗標發行, 2021. Print.
6. 岡田佑一, 鄧瑋敦, and 博碩文化 編譯. Short Coding寫出簡捷好程式 : 短碼達人的心得技法. 初版. 臺北縣汐止市: 博碩文化出版, 2008. Print.
7. 冼鏡光. 名題精選百則 技巧篇. 第三版. 臺北市: 儒林圖書公司, 2010. Print.
8. 冼鏡光. 名題精選百則 技巧篇使用C語言. 第二版. 臺北市: 儒林圖書, 2002. Print.
9. 冼鏡光. 名題精選百則. 技巧篇: 使用C語言. 三版. 臺北市: 格致出版, 1996. Print.
10. 增井敏克., and 許郁文. 培養刷題基本功: Python程式設計師的頭腦體操. 初版. 臺北市: 碁峰資訊, 2021. Print.
11. 付東來. 刷題實戰筆記: 演算法工程師求職加分的祕笈. 初版. 新北市: 博碩文化, 2021. Print.
