# Computer Architecture notes

collect and note by : JingShing

## Chapter 1

## Dialog目錄

[1.1 介紹](#1-1-Abstraction)

1.2 計算機架構中的八大理念

1.3 你的程式之下

1.4 覆蓋之下

1.5 建構處理器與記憶體的技術

1.6 效能

1.7 功耗障壁

1.8 巨變：由單處理器轉移至多處理器

1.9 實例：測試Intel core i7

1.10 謬誤與陷阱

### 1-1 Abstraction

* 計算機抽象化(Abstraction)
  * 以精要的形式來表達計算機的內涵、概念、特質、屬性或意義等，這個從計算機本身找出這個精要的形式的過程就是計算機抽象化。

* 計算機是極為快速變化的資訊科技工業中的產物

  * 如果運輸業有計算機工業的進展速度，今天我們將大約可以花幾分錢以一秒從紐約到倫敦。

  * 這個不尋常的工業以令人驚異的速度接納創意

### 計算應用的種類與它們的特性

大體而言，計算機被運用在三個不同種類的應用：

* 個人型計算機(Personal computers, PCs)

  * 強調以<u>**低成本**</u>提供單一使用者不錯的效能並能執行其他公司的軟體

* 伺服器(servers)

  是昔日大型主機、迷你計算機及超級電腦的現代版，通常經由網路來使用

  * 提供計算及輸出入容量上更大的擴充性
  * 也強調可靠度
  * Range from small servers to building sized

* 嵌入式計算機(embedded computers)

  在應用與效能的範圍最廣

  * 設計來執行單一應用或一組相關的應用，該等應用一般與硬體整合在一起，以單一系統型態呈現

  * 大部分使用者從不知道他們正在使用這類計算機通常有其獨特的應用需求以及最低效能和嚴格的成本與功耗限制

  * 通常更不能容忍失效

  * 經由簡單化或冗餘(redundancy)技術來達成


  > 冗餘(redundancy) : 利用多個 mcu 做溝通，作為備用
  > mcu : memory + cpu + io
  >
  > examples : 車載電腦、物聯網

### 進入後個人電腦時代

* 個人行動裝置(personal mobile device, PMD)由電池驅動、無線聯線至網際網路且一般售價為數百美元

  * 和個人電腦一樣，使用者可於其上執行可下載的軟體(“apps”)
  * 可能使用觸控螢幕甚或語言輸入

* 庫房規模計算機(Warehouse Scale Computers, WSCs)

  * Scalable可擴充

  * Distributed可分散

  * Cost efficiency

    > 單一硬盤損毀時可還原資料，資料會備份到多個硬盤

  ​	![wcs_overview](pictures/wscs_overview.png)

  雲端計算(Cloud Computing)

  * 軟體寫作者常常會將他們的應用程式一部分執行於個人行動裝置上而一部分執行於雲端

  > 相較於雲端計算，本地的計算稱為邊緣計算(local)。

  

> 22/9/14

