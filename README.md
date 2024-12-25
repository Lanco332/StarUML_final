# 南華大學軟體工程-期末報告-如何畫出一張優秀的架構圖（4+1模式）
## 組員:11124233黃文龍 11125005林啟陽

## 一、先釐清一些基礎概念
### 什麼是架構？

    架構就是對系統中的實體以及實體之間的關係所進行的抽象描述，是一系列的決策。

    架構是結構和願景。系統架構是概念的體現，是對物件/資訊的功能與形式元素之間的對應情況所做的分配，是對元素之間的關係以及元素與周邊環境之間的關係所做的定義。

    做好架構是一個複雜的任務，也是個很大的話題，本文就不深入探討。有了架構之後，就需要讓相關方理解並遵循相關決策。

### 什麼是架構圖？

    系統架構圖是用來抽象地表示軟體系統的整體輪廓及各個組件之間的相互關係和約束邊界，還有軟體系統的物理部署與演進方向的整體視圖。

### 架構圖的作用

    一圖勝千言。為了讓相關方理解並遵循架構決策，需要將架構資訊傳遞出去，而架構圖是一個非常好的載體。

    因此，繪製架構圖的目的是：

    解決溝通障礙
    達成共識
    減少歧義
## 二、架構圖分類

搜集了很多資料，分類有很多，其中一種比較流行的是 4+1 視圖，分別為場景視圖、邏輯視圖、物理視圖、處理流程視圖和開發視圖。

### 1.場景視圖
場景視圖用於描述系統的參與者與功能用例之間的關係，反映系統的最終需求和交互設計，通常由用例圖來表示。
![image](https://github.com/Lanco332/staruml_1/blob/main/picture/1.jpg)

### 2.邏輯視圖
邏輯視圖用於描述系統軟體功能拆解後的組件關係、組件約束和邊界，反映系統整體組成與系統如何構建的過程，通常由 UML 的組件圖和類圖來表示。

![image](https://github.com/Lanco332/staruml_1/blob/main/picture/1.jpg)

### 3.物理視圖
物理視圖用於描述系統軟體到物理硬體的映射關係，反映出系統的組件如何部署到一組可計算的機器節點上，用於指導軟體系統的部署實施過程。

![image](https://github.com/Lanco332/staruml_1/blob/main/picture/1.jpg)

### 4.處理流程視圖
理流程視圖用於描述系統軟體組件之間的通信時序、數據的輸入輸出，反映系統的功能流程與數據流程，通常由時序圖和流程圖來表示。

![image](https://github.com/Lanco332/staruml_1/blob/main/picture/1.jpg)

### 5.開發視圖
開發視圖用於描述系統的模組劃分和組成，以及細化到內部包的組成設計，服務於開發人員，反映系統開發實施過程。

![image](https://github.com/Lanco332/staruml_1/blob/main/picture/1.jpg)

    以上 5 種架構視圖從不同角度表示一個軟體系統的不同特徵，組合在一起作為架構藍圖來描述系統架構。
## 三、怎樣的架構圖是好的架構圖

在畫出一個好的架構圖之前，首先應該要明確其受眾，並想清楚需要向他們傳遞什麼信息。
因此，不應該僅僅為了畫一個物理視圖而畫物理視圖，或者為了畫邏輯視圖而畫邏輯視圖，而是要根據受眾的不同和需要傳遞的信息不同，用圖準確地表達出來。最後的圖可能會落在這些分類中，但這應該是結果而不是目的。
那麼，判斷畫出的圖是否好的一個直接標準就是：受眾是否準確接收到想要傳遞的信息。
明確這一點後，從受眾角度來說，一個好的架構圖應該是不需要解釋的，它應該是自描述的，並且具備一致性和足夠的準確性，能夠與代碼相呼應。
畫架構圖遇到的常見問題
### 方框代表什麼？
隨意使用方框、圓形或其他形狀可能會引起混淆，例如：

    虛線和實線是什麼意思？箭頭的含義是什麼？顏色有什麼特別含義嗎？
    隨意使用線條或箭頭也可能引起誤會。

    運行時與編譯時的衝突？層級衝突？
    架構是一項複雜的工作，只使用單一圖表來表示架構很容易造成語義上的混亂。
## 四、本文推薦的畫圖方法
C4 模型使用容器（應用程式、數據存儲、微服務等）、組件和代碼來描述一個軟體系統的靜態結構。

這些圖容易繪製，並給出了畫圖的要點。但更關鍵的是，它明確指出了每種圖可能的受眾以及意義。

## 案例：來自 C4 模型的示例
### 1.語境圖（System Context Diagram）

![image](https://github.com/Lanco332/staruml_1/blob/main/picture/1.jpg)

這是一個想像中的互聯網銀行系統，它使用外部大型機銀行系統來存取客戶賬戶與交易信息，並通過外部電郵系統向客戶發送郵件。

這樣的圖非常簡單、清晰，甚至不需要過多解釋就能理解。它包含了待建設的系統本身、系統的用戶，以及與該系統交互的周邊系統。

#### 語境圖可以回答以下問題：

要構建的系統是什麼？
它的用戶是誰，誰會使用它？
它如何融入已有的 IT 環境？
如何繪製？

    圖中央是自己的系統，周圍是用戶和其他與之交互的系統。
    核心是梳理清楚待建設系統的用戶和高層次的依賴。
    梳理清楚後，繪製只需要幾分鐘時間。
### 2.容器圖（Container Diagram）
容器圖是在語境圖的基礎上，將待建設的系統進行展開，描述系統內部的主要容器（應用程式、數據存儲等）及其相互作用。

![image](https://github.com/Lanco332/staruml_1/blob/main/picture/1.jpg)

在圖中，除了使用者和周邊系統，待建設的系統包括以下內容：

    一個基於 Java/Spring MVC 的 Web 應用，作為系統功能的入口。
    一個基於 Xamarin 架構 的手機應用，提供手機端功能入口。
    一個基於 Java 的 API 應用，提供服務支持。
    一個 MySQL 資料庫 用於存儲資料。
各個應用之間的交互在箭頭線上清楚地標註了說明。
圖中的觀察點
查看這張圖時，觀眾往往不會過多關注以下細節：

    是直角方框還是圓角方框。
    是實線箭頭還是虛線箭頭。
    箭頭的具體指向。
    即使有許多畫圖方式對框和線的含義進行了定義，這也要求畫圖者和觀圖者都需要清楚地理解這些定義，才能完整地讀取圖中的信息。但在現實中，這樣的要求通常過高，因此很多圖只能傳遞大概的含義。

#### 圖的受眾與用途
這張圖的受眾可以是：

團隊內部或外部的開發人員。
運維人員。
圖的用途包括：

展現軟體系統的整體形態。
體現高層次的技術決策。
展示系統中的職責如何分佈，容器之間如何交互。
指導開發者在哪裡撰寫程式碼。
#### 如何繪製
    用一個框圖來表示。
    框內可能包括名稱、技術選擇、職責等信息。
    框之間的交互需要清晰地標註。
    如果涉及外部系統，建議明確邊界。
### 3.組件圖（Component Diagram）
組件圖將某個容器進一步展開，描述其內部的模組。

![image](https://github.com/Lanco332/staruml_1/blob/main/picture/1.jpg)

#### 主要用途：

描述系統由哪些組件/服務組成。
梳理組件之間的關係與依賴。
為軟體開發的分解與交付提供框架。
這些圖主要是為內部開發人員設計，用於指導程式碼的組織與構建。

### 4.類圖（Code/Class Diagram）
類圖主要針對技術人員，較為常見，本文不再詳細介紹。

![image](https://github.com/Lanco332/staruml_1/blob/main/picture/1.jpg)
## 五、案例分享
以下是一個內部實時數據工具的架構圖，作為應該自描述的架構圖，這裡不再做過多解釋。如果有地方看不明白，那麼一定是圖還畫得不夠好。

![image](https://github.com/Lanco332/staruml_1/blob/main/picture/1.jpg)

## 六、總結
畫好架構圖可能有許多方法論，本篇介紹的主要是 C4 模型。C4 的理論也是不斷演化的。

但不論使用哪種方法論，我們回到畫圖的初衷：為了更好的溝通。在畫圖的過程中，不需要被條條框框所限制。

簡而言之，畫之前想清楚：畫圖給誰看、看什麼，以及如何做到不解釋也能看懂。
