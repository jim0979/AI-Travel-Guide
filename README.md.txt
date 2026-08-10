# 🌸 花蓮觀光導覽

一個以花蓮旅遊為主題的觀光導覽網站，提供景點瀏覽、我的收藏以及管理後台等功能。

本專案使用前端網頁技術搭配 Flask 後端與 SQLite 資料庫，實作網站資料管理與管理員登入功能。

---

## 📌 專案介紹

本專案主要提供使用者一個簡單、直覺的花蓮旅遊導覽平台。

使用者可以透過網站瀏覽花蓮各地景點，並使用收藏功能管理自己感興趣的景點。

另外建立管理後台，讓管理員可以登入系統並進行景點資料的管理。

---

## ✨ 主要功能

### 🏞️ 景點導覽
- 瀏覽花蓮旅遊景點
- 顯示景點圖片與相關資訊
- 依照景點資料進行瀏覽

### ❤️ 我的收藏
- 收藏喜歡的旅遊景點
- 查看已收藏的景點
- 管理個人的收藏內容

### 🔐 管理員登入
- 管理員登入驗證
- Session 登入狀態管理
- 防止未登入使用者直接進入管理後台

### 🛠️ 景點管理
- 管理景點資料
- 新增景點
- 修改景點
- 刪除景點

---

## 🧰 使用技術

### Frontend
- HTML5
- CSS3
- JavaScript
- Vue.js
- Bootstrap

### Backend
- Python
- Flask

### Database
- SQLite

### Development Tools
- Visual Studio Code
- Git
- GitHub

---

## 📁 專案結構

```text
期末/
│
├── app1.py                  # Flask 後端程式
├── 花蓮.json                # 花蓮景點資料
├── README.md                # 專案說明文件
├── .gitignore               # Git 忽略檔案設定
│
├── frontend/                # 前端網站
│   ├── index.html           # 首頁
│   ├── favorite.html        # 我的收藏
│   ├── admin_login.html     # 管理員登入
│   ├── manage.html          # 管理頁面
│   ├── welcome.html         # 歡迎頁面
│   │
│   ├── css首頁/             # CSS 樣式
│   ├── jss/                 # JavaScript / Vue
│   ├── images1/             # 網站圖片
│   └── js資料/              # JSON 資料
│
└── venv/                    # Python 虛擬環境