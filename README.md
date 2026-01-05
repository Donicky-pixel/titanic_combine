# 🚢 Titanic Docker 專案（前後端＋資料庫整合）

本專案使用 **Docker + Docker Compose**，整合：

- MySQL（Titanic 資料庫）
- Flask API（後端）
- HTML 前端頁面（顯示 Titanic 資料）

👉 只要一行指令，即可在任何電腦啟動並打開網頁。

---

## 📦 專案結構

```text
titanic_project/
├─ docker-compose.yml
├─ python_folder/
│  ├─ Dockerfile
│  ├─ pymysql_flask.py
│  └─ static/
│     └─ index.html
└─ db/
   └─ init/
      └─ 01_titanic_dump.sql

docker --version
docker compose version

step 1
git clone <你的 GitHub Repo URL>
cd <Repo 資料夾名稱>

step2
docker compose up -d --build
看到沒有 error 就代表成功。

step3
docker compose ps
應該看到：
MySQL：healthy
Flask：Up

step4 檢查api有無回應
curl http://localhost:5000/titanic




