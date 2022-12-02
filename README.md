**小組作業1** : 
顯示在小組的github上，請列出專案的
- 組長與組員之姓名
- 個別組員的任務
- 專題題目
- 內容
- 甘特圖與PERT/CPM圖 (期限: A班 10/10 , B班10/11)

## 專案組別: 9

### 組員介紹與分工

|     第9組     |  姓名  |                   個別任務                   |
| :------------: | :----: | :------------------------------------------: |
| **組長** | 林澤權 | 題目構想、流程設計、功能構想、後端開發、測試 |
|      組員      | 潘沛儀 |    需求構想、市場調查、前端開發、企劃發想    |
|      組員      | 李翊翎 |    需求構想、市場調查、前端開發、企劃發想    |
|      組員      | 陳宥諺 |          資料庫設計、後端開發、測試          |
|      組員      | 林貞智 |         題目構想、功能構想、後端開發         |


---

## week4小組作業1 : 

### 專題題目

- 失蹤人口分析與找尋(暫定)
- 車輛拖吊分析與找尋

### 內容

1. 依據[國家人口失蹤資料集為來源](https://data.gov.tw/dataset/14420)，可以透過其資料集，分析年齡層、失蹤性別、地區比例等... 提供相關研究人員參考
2. 透過平台，可以依據失蹤地點、特徵、年齡、時間去篩選可能的人選

### 甘特圖



- mermaid繪製版本

```mermaid

gantt
    title 第九組小組作業甘特圖

    section 第一階段
    題目構想     :a1, 2022-10-4, 7d
    需求構想     :a2,after a1  , 8d
    功能構想     :a3 , after a2  , 6d
    section 第二階段
    市場分析     :b1, 2022-11-1, 8d
    客群分析     :b2, after b1, 8d
    評估可行性   :b3, after b2  , 8d
    section 第三階段    
    前端開發      :c1,after b3 , 12d
    資料庫建立      :c2 ,after b3, 12d
    後端開發	:c3 ,after b3, 12d
    section 第四階段    
    系統整合:d1,2022-12-2 , 7d
    測試、修改: d2, after d1 , 10d
    成品展示:d3, after d2 , 5d
  
```

### PERT/CPM圖

- google繪製版本
![image2](https://user-images.githubusercontent.com/57654809/194913530-bee24e8f-ccb6-407b-832b-d13519a7ea62.png)

- mermaid繪製版本

[PERT圖繪製版本連結](https://hackmd.io/@cjqBX7RDSMSJUP0adJLUmw/rkDcmRbmj)
![image1](https://user-images.githubusercontent.com/57654809/194921178-9523aca4-c214-4174-aa56-570bd8a2b2ea.png)


---

## week6小組作業2: 

### 功能性需求與非功能性需求

- **功能性需求**
    1. 失蹤人物資料查詢
    2. 失蹤情況分類及分析
    5. 後台管理介面

- **非功能性需求**
    1. 反應性: 24小時提供使用者查詢資料並且快速查詢
    2. 使用性: UI介面清楚、功能簡約明瞭
    3. 可靠度: 資料可自動備份、自訂系統資料排序方式
    4. 效能: 2秒內至少能夠載入100筆資料
    5. 維護性: 能夠控制資料
    
### 呈現功能分解圖(functional decomposition diagram, FDD)

```mermaid
flowchart TB;

main[專案 - 失蹤人口分析與找尋系統]
a1[1. 資料查詢系統]
    a1-->a1-1[發生年份]
    a1-1-->a1-2[失蹤當時特徵]
    a1-2-->a1-3[失蹤人物的回報]

a2[2. 分析系統]
a2-->a2-1[失蹤人口統計分類]

    a2-1-->a2-2[人口區域分析]
    a2-1-->a2-3[各時間統計分析]
    a2-1-->a2-4[年齡分布統計]
    a2-1-->a2-5[依失蹤原因統計]

    a3[3. 後台管理系統]
    a3-->a3-0[失蹤概況管理]
    a3-->a3-1[失蹤名單管理]

main-->a1;
main-->a2;
main-->a3;


```

### 寫出需求分析的文字描述

**一個人口失蹤分析與查詢的網站的需求分析如下:**

- **管理者**
    - 可以依據失蹤對象的資訊去分類
    - 可以針對使用者失蹤對象的對照找到該對象
    - 更新失蹤人口名單資料

- **使用者**
    - 可以依據對象失蹤的發生時間及特徵去做查詢
    - 可以選擇統計圖的呈現樣式
    - 可以依據失蹤對象進行類別篩選
    - 篩選類別可以為時間、地區、原因等
    - 使用者回報網站失蹤對象詳細資訊
- 
### 劃出三個以上的使用案例說明及使用案例圖

**使用案例圖**

![Blank diagram](https://user-images.githubusercontent.com/57654809/198653715-8f555c5a-e2c6-4036-ac7f-bf0f2227184e.png)



**查詢系統**

使用案例說明:

| 使用案例名稱 |  資料查詢系統 |
| --- | --- |
| 行動者 | 使用者 |
| 說明 | 依據所需條件查詢失蹤對象 |
| 完成動作 | 1. 選擇發生時間 2.選擇地點 3. 說明特徵 4. 提交表單 5. 顯示查詢結果 6.選擇是否通報失蹤對象的資訊及情況 |
| 替代方法 | 1. 選擇發生時間 2.選擇地點 3. 說明特徵 4. 提交表單 5. 查無結果，選擇通報失蹤 |
| 先決條件 | 失蹤時間跟地點至少選擇一項 |
| 後置條件 | 確認條件後送出並依照資訊查詢結果，並選擇是否通報失蹤對象的資訊及情況 |
| 假設 |  |

**分析系統**

使用案例說明:

| 使用案例名稱 | 分析系統 |
| --- | --- |
| 行動者 | 使用者 |
| 說明 | 依據失蹤人口的條件及選擇呈現方式去顯示該條件的數據 |
| 完成動作 | 1. 選擇條件(性別、年齡、區域、發生時間、查獲情況) 2. 選擇呈現方式(文字雲、多項統計圖) 3. 依據選擇條件顯示結果 |
| 替代方法 | 1. 選擇條件(性別、年齡、區域、發生時間、查獲情況) 2. 選擇呈現方式(文字雲、多項統計圖) 3. 回傳資料有誤 |
| 先決條件 | 條件至少選擇一項，並必須選擇呈現方式 |
| 後置條件 | 條件及呈現方式都選擇後，即可回傳結果 |
| 假設 | 無 |

**管理系統**

使用案例說明:


| 使用案例名稱 | 後台管理系統 |
| --- | --- |
| 行動者 | 管理者 |
| 說明 | 管理者可依據失蹤概況管理，並管理失蹤人口的名單及目前情形，依據失蹤名單比對是否跟使用者通報相同 |
| 完成動作 | 1.依據失蹤概況管理 2.確認失蹤人口是否已找到 3.依據失蹤名單管理 4.確認名單內容與使用者回報相同 |
| 替代方法 | 1.依據失蹤概況管理 2.確認失蹤人口是否已找到 3.失蹤人口資料不符，通報回傳錯誤資料 4.依據失蹤名單管理  5.確認名單內容與使用者回報相同 6.失蹤人口資料不符，通報回傳錯誤資料 |
| 先決條件 | 進入後台後，選擇欲管理名單，接著查詢有無使用者回報資訊|
| 後置條件 | 若有使用者回報資訊，則針對該名單進行修改|
| 假設 |  |


### 使用Figma劃出第一個使用案例的動態模擬畫面
[第一個使用案例_Figma模擬畫面](https://www.figma.com/proto/tbNNRC62j8YFIBvhxEDdcL/team9?node-id=11%3A117&scaling=scale-down&page-id=0%3A1)

---

## week7小組作業3 : 

### 作業3內容 系統環境圖及圖0: 
![DFD](https://user-images.githubusercontent.com/57654809/198677743-8b13c8b5-8c54-4f43-ac78-f01e260754b6.png)


---

## week8小組作業4:

### 類別圖

<img width="591" alt="image" src="https://user-images.githubusercontent.com/57654809/199747742-21ac9cff-bc71-4fdc-b6ff-5137769d039a.png">

### 使用案例1 - 資料查詢系統

- 循序圖

<img width="433" alt="image" src="https://user-images.githubusercontent.com/57654809/199748705-5f11885a-1af3-47c8-9519-52070a6272ca.png">

- 活動圖

<img width="571" alt="image" src="https://user-images.githubusercontent.com/57654809/199748757-dd513df7-7187-46c8-ace4-1ae769ebf570.png">


### 使用案例2 - 分析系統

- 循序圖

```mermaid
sequenceDiagram
使用者->>+分析系統:選擇條件(性別、年齡、區域、發生時間、查獲情況)
activate 使用者
deactivate 使用者
activate 分析系統
deactivate 分析系統
使用者->>+分析系統:選擇呈現方式(文字雲、多項統計圖)
activate 使用者
deactivate 使用者
activate 分析系統
deactivate 分析系統
分析系統-->>-使用者:顯示結果
activate 使用者
deactivate 使用者
activate 分析系統
deactivate 分析系統
```

- 活動圖
![image](https://user-images.githubusercontent.com/113969847/200119822-d22c36f7-9f12-43eb-aa66-14b000715521.png)

### 使用案例3 - 後台管理系統

- 循序圖
<img width="475" alt="nkust" src="https://user-images.githubusercontent.com/113968421/200969385-def9c9ba-398d-44f7-91ca-495da714ff82.png">


- 活動圖

![實用案例3_活動圖](https://user-images.githubusercontent.com/113968421/200120359-2ecf9920-dcb1-41d5-92eb-17599aabf8c3.jpg)



---
## week7小組　作業5

<img width="622" alt="image" src="https://user-images.githubusercontent.com/57654809/205289494-a84d0f88-2a9a-40b8-811e-77278ab15afa.png">
<img width="621" alt="image" src="https://user-images.githubusercontent.com/57654809/205289444-8ec9b21a-edc7-4141-975c-40859db12917.png">
<img width="619" alt="image" src="https://user-images.githubusercontent.com/57654809/205289533-985960df-3d37-43fb-8028-d119d1a87f57.png">
<img width="618" alt="image" src="https://user-images.githubusercontent.com/57654809/205289565-e0adb690-b3fb-4163-a59c-03a41cf7f7d2.png">




