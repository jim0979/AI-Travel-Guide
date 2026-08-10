# 🌸 花蓮觀光導覽系統 (Hualien Travel Guide System)

一個以花蓮旅遊為主題的觀光導覽響應式網站，整合前台景點流暢瀏覽、精緻彈窗詳情、個人化收藏管理，以及擁有身分驗證機制的後台資料管理系統。

本專案採用前後端分離架構，使用輕量網頁技術搭配 **Flask** 後端核心與 **SQLite** 關聯式資料庫，實作了完整的 **CRUD** 資料管理與後台管理員功能。

---

## 📌 專案介紹

本專案主要提供使用者與系統管理員一個直覺、流暢且安全的花蓮旅遊導覽暨維護平台。

* **對於一般遊客**：能透過精美、高質感的介面跨裝置探索花蓮各地景點，並可即時將心儀的景點加入個人收藏清單，提供客製化的行程規劃輔助。
* **對於系統管理員**：系統內建身分驗證防護牆。管理員必須先通過登入驗證，才能進入專屬的圖表維護後台，進行景點資料的動態新增、編輯、刪除與全區數據分佈統計。

---

## ✨ 主要功能

### 🏞️ 景點探索與導覽
- **滿版形象橫幅**：頂端具備沉浸式大圖與主題情境標籤（山海秘境、花蓮美食等），點擊快速聚焦。
- **關鍵字即時搜尋**：可輸入景點名稱或行政區等關鍵字，系統會即時過濾並動態篩選符合的景點。
- **彈性分頁控制**：支援自訂每頁顯示的景點數量（如：一次顯示 6 筆），避免海量資料造成頁面擁擠。
- **非同步詳情彈窗 (Modal)**：點擊「了解更多」即時彈出精緻光箱，免切換頁面即可瀏覽開放時間、門票、地址等結構化資訊，並整合 **Google 地圖導航**。

### ❤️ 我的收藏管理 (`favorite.html`)
- **開關式動態收藏**：景點卡片與詳情彈窗內建愛心按鈕，點擊可即時高亮（紅色實心）或取消收藏。
- **個人化收藏清單**：擁有專屬頁面加載目前收藏，標題會動態統計當前收藏總數（如：我的收藏景點 (3)）。
- **收藏內二次搜尋**：收藏頁面貼心提供專屬搜尋框，方便使用者在眾多收藏中二次過濾。
- **時間戳記追蹤**：卡片底部會精準顯示該景點被加入收藏的具體時間。

### 🔐 管理員安全登入 (`admin_login.html`)
- **權限防護隔離**：在進入管理後台前設定登入驗證關卡，非授權使用者無法直接存取維護頁面。
- **後端狀態管理**：後端結合 Flask Session 機制，嚴格校驗管理員的登入狀態與通行憑證。
- **友善導航連結**：介面貼心提供「返回花蓮觀光導覽」捷徑，方便管理員隨時返回前台測試或瀏覽。

### 🛠️ 景點資料維護後台 (`manage.html`)
- **高效率雙欄佈局**：在同一畫面中完美串聯「資料新增表單」與「清單管理表格」，大幅提升維護效率。
- **智慧表單校驗**：欄位具備紅色星號（`*`）必填提示與灰色預設引導文字，支援一鍵確認新增與表單清空。
- **即時總量統計**：後台即時動態顯示系統內目前建立的景點總筆數（如：目前共 11 個景點）。
- **全功能 CRUD 維護**：管理列表內建「📝 編輯」與「🗑️ 刪除」一鍵式快速操作按鈕，與後端資料庫全面連動。

### 📊 數據視覺化統計
- **動態長條圖表**：後台成功整合前端圖表控制元件，將資料庫中的景點按「行政區（鄉鎮市）」進行分組歸納。
- **數據即時回饋**：直觀展示各區域的景點分佈數量，協助掌握旅遊資源密度。

---

## 📸 系統介面展示 (Screenshots)

### 🌅 景點清單頁 - 頂端視覺橫幅
採用高品質的花蓮海濱落日風景搭配動態標語，營造出沉浸式的旅遊導覽入口。
<img width="1911" height="1028" alt="首頁_0" src="https://github.com/user-attachments/assets/e1138011-50f8-4816-b380-b981e6df8469" />

### 📱 跨裝置響應式網頁設計 (RWD Support)
本系統前端介面具備完整的 RWD 適應能力，針對不同裝置的螢幕寬度進行了專屬的佈局優化：
* **🖥️ 桌機寬度 (Desktop View)**：景點列表自動切換為**流暢的三欄並排卡片**，頂端導覽列呈現完整的寬螢幕文字選單，視覺感開闊、平衡。

<img width="1296" height="1043" alt="桌機寬度1200px_0" src="https://github.com/user-attachments/assets/a6349c20-e564-48f3-b5ad-23523bbd1ed2" />


* **📱 平板寬度 (Tablet View)**：景點卡片自動調整為**雙欄並排佈局**，兼顧閱讀舒適度與網頁排版。

<img width="814" height="1037" alt="平板寬度768px_0" src="https://github.com/user-attachments/assets/ecb1f7f6-80a6-417a-827c-4db80f2e45d3" />


* **📞 手機寬度 (Mobile View)**：選單自動收納為單一的**漢堡選單按鈕**，景點列表則改為單欄垂直排列，方便單手滑動操作。
<img width="641" height="723" alt="手機寬度375px_0" src="https://github.com/user-attachments/assets/f75a193c-d172-445e-acb8-671f447eb549" />


### 🔍 景點詳細資訊彈窗 (Attraction Detail Modal)
採用彈出式視窗 (Modal) 技術，整合圖示元素分欄清晰呈現：開放時間、門票資訊、聯絡電話、景點地址以及深度文字介紹，並內建 Google 地圖導航快捷鍵。
<img width="897" height="841" alt="景點詳細內容_0" src="https://github.com/user-attachments/assets/7ecfdcac-57b5-4a4b-9dcd-0c2aecdab830" />

### ❤️ 我的收藏頁面 (`favorite.html`)
即時顯示目前收藏清單，具備動態計數、收藏內搜尋框以及明確的時間戳記紀錄。
<img width="1843" height="1025" alt="我的收藏_0" src="https://github.com/user-attachments/assets/a2878769-45fd-4086-a98b-1312cd1814d8" />

### 🔐 管理員安全登入頁面 (`admin_login.html`)
採用高質感的雙欄卡片風格，左側展示「探索花蓮，山海之間的美好」專案品牌，右側提供內建圖示的「管理員帳號」與「管理員密碼」安全輸入表單。
<img width="1268" height="796" alt="管理者登入畫面" src="https://github.com/user-attachments/assets/748bbc06-34df-4d57-bdbe-707f20a1929f" />

### 🛠️ 景點資料管理後台 (`manage.html`)
高效率雙欄管理介面，左側為新增表單，右側為內建「編輯/刪除」與專屬搜尋框的景點管理清單。
<img width="1727" height="984" alt="景點管理_0" src="https://github.com/user-attachments/assets/6a7b25cc-6045-42c2-bbca-41586a120a0c" />

### 📊 資料視覺化統計與專業頁尾
利用直觀的長條圖（Bar Chart）動態呈現花蓮各個鄉鎮區域（如：壽豐鄉、吉安鄉等）目前的景點數據。下方整合深色專業頁尾，包含快速連結與聯絡資訊。
<img width="1876" height="713" alt="統計圖表_0" src="https://github.com/user-attachments/assets/d864c93d-7a54-456e-a995-e344a999da45" />

---

## 🗄️ 資料庫設計 (Database Schema)

系統採用 **SQLite** 進行資料儲存與持久化管理，以下為核心資料表設計：

### 1. `favorites` 收藏資料表
用於記錄使用者與景點之間的收藏關聯。

| 欄位名稱 (Field) | 資料型態 (Type) | 約束條件 (Constraints) | 說明 (Description) |
| :--- | :--- | :--- | :--- |
| `id` | `INTEGER` | PRIMARY KEY, AUTOINCREMENT | 收藏紀錄流水號 |
| `user_id` | `TEXT` | NOT NULL | 使用者識別碼（未登入預設為 `guest`） |
| `attraction_id` | `TEXT` | NOT NULL, FOREIGN KEY | 關聯之景點 ID (對應景點表 `id`) |
| `collected_at` | `DATETIME` | DEFAULT CURRENT_TIMESTAMP | 加入收藏的具體時間 |

---

## 🌐 API 介面規格 (API Endpoints)

本專案後端全面採用 **RESTful API** 架構設計，以下為經由 Postman 完整測試通過的核心介面規範：

### 1. 獲取所有景點清單 (Get All Attractions)
* **HTTP 請求方法**：`GET`
* **API 路徑**：`/api/attractions`
* **回應結果 (Response - 200 OK)**：
  ```json
  {
    "attractions": [
      {
        "id": "HL-ATT-001",
        "title": "太魯閣國家公園 (燕子口步道)",
        "category": "自然峽谷/步道探險",
        "region": "花蓮縣秀林鄉",
        "description": "燕子口步道為太魯閣峽谷的精華路段...",
        "image_url": "images1/image_燕子口步道ai.png",
        "created_at": "2026-07-29T10:00:00Z"
      }
    ]
  }
  ```

### 2. 景點收藏與取消狀態管理 (Toggle Favorite)
* **HTTP 請求方法**：`POST`
* **API 路徑**：`/api/favorite`
* **請求格式 (Payload - JSON)**：
  ```json
  {
    "id": "user_guest",
    "attraction_id": "HL-ATT-001"
  }
  ```
* **情境 A：新增景點收藏 (Add to Favorites)**
  * **回應結果 (200 OK)**：
    ```json
    {
      "message": "已加入收藏",
      "status": "favorited"
    }
    ```
* **情境 B：取消指定收藏 (Remove from Favorites)**
  * **回應結果 (200 OK)**：
    ```json
    {
      "message": "已取消收藏",
      "status": "unfavorited"
    }
    ```

### 3. 查詢指定使用者收藏清單 (Get User Favorites)
* **HTTP 請求方法**：`GET`
* **API 路徑**：`/api/favorites/<user_id>`
* **測試範例路徑**：`/api/favorites/user_guest`
* **回應結果 (Response - 200 OK - 清單為空時)**：
  ```json
  {
    "favorites": [],
    "user_id": "user_guest"
  }
  ```

### 4. 新增旅遊景點 (Create New Attraction)
後端會自動產生唯一的 UUID（如 `HL-ATT-1786084104`）並針對未傳入欄位給予標準智慧預設值。
* **HTTP 請求方法**：`POST`
* **API 路徑**：`/api/attractions`
* **請求格式 (Payload - JSON 範例)**：
  ```json
  {
    "title": "456",
    "region": "789"
  }
  ```
* **回應結果 (Response - 201 Created)**：
  ```json
  {
    "attraction": {
      "id": "HL-ATT-1786084104",
      "title": "456",
      "region": "789",
      "category": "自然風景",
      "description": "",
      "image_url": "https://unsplash.com",
      "created_at": "2026-08-07 14:28:24"
    },
    "message": "成功新增景點"
  }
  ```

### 5. 刪除指定景點 (Delete Attraction)
* **HTTP 請求方法**：`DELETE`
* **API 路徑**：`/api/attractions/<attraction_id>`
* **測試範例路徑**：`/api/attractions/HL-ATT-1786084104`
* **回應結果 (Response - 200 OK)**：
  ```json
  {
    "message": "已成功刪除景點"
  }
  ```

---

## 🧰 使用技術

### Frontend
- **HTML5 / CSS3 / JavaScript (ES6+)**：核心前端骨架與基礎樣式。
- **Vue.js**：實現雙向資料綁定，動態渲染景點卡片、搜尋過濾、分頁、登入表單綁定及收藏狀態。
- **Bootstrap**：提供響應式柵格系統 (Grid) 與 Modal 彈窗元件。
- **Data Visualization Library**：後台報表數據視覺化渲染。

### Backend
- **Python 3**：核心開發語言。
- **Flask**：輕量級 Web 框架，提供路由派發與建立 RESTful API。
- **Session 管理**：實作管理員安全登入與狀態憑證管理，進行後台路由重導向攔截保護。

### Database
- **SQLite**：內嵌式關聯型資料庫，負責景點與收藏資料的安全持久化。

### Development Tools
- **Visual Studio Code**：核心代碼編寫與除錯。
- **Postman**：後端 RESTful API 介面嚴謹測試。
- **Git / GitHub**：版本控制、變更管理與遠端程式碼託管。

---

## 📁 專案結構

```text
期末/
│
├── app1.py                  # Flask 後端主程式 (API 路由與資料庫互動)
├── 花蓮.json                # 花蓮初始景點資料庫備份檔
├── README.md                # 專案說明文件 (本文件)
├── .gitignore               # Git 忽略檔案設定
│
├── frontend/                # 前端靜態網站資源
│   ├── index.html           # 前台首頁 / 景點導覽與分頁搜尋
│   ├── favorite.html        # 我的收藏頁面
│   ├── admin_login.html     # 管理員安全登入頁面
│   ├── manage.html          # 管理後台 / 雙欄維護與圖表統計
│   ├── welcome.html         # 網站導覽歡迎首頁
│   │
│   ├── css首頁/             # 全站介面與網頁控制樣式表
│   ├── jss/                 # 前端邏輯控制與 Vue 核心實作
│   ├── images1/             # 景點視覺圖檔與品牌資產
│   └── js資料/              # 靜態本地 JSON 資料快照
│
└── venv/                    # Python 虛擬環境 (套件相依性隔離)
```
