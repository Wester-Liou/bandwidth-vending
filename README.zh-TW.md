# Bandwidth Vending | 流量變現

將您閒置的網路頻寬轉化為被動收入。本專案使用 Docker 快速部署多個流量變現應用程式 (Honeygain, PacketStream, Pawns.app, TraffMonetizer)。

[English README](README.md)

## 💰 開始賺錢 (推薦連結)

使用以下連結註冊可獲得獎勵 (同時支持本專案)：

- **Honeygain**: [加入 Honeygain](https://join.honeygain.com/EFG20FAEB3)
- **PacketStream**: [加入 PacketStream](https://packetstream.io/?psr=7r2e)
- **Pawns.app**: [加入 Pawns.app](https://pawns.app/?r=18988103)
- **TraffMonetizer**: [加入 TraffMonetizer](https://traffmonetizer.com/?aff=2099471)

## 🚀 包含服務

- **Honeygain**: 分享網路頻寬用於數據情報。
- **PacketStream**: P2P 住宅代理網絡。
- **Pawns.app (前身為 IPRoyal Pawns)**: 分享網路進行調查和其他任務。
- **TraffMonetizer**: 變現您的流量。
- **Watchtower**: 自動更新正在運行的 Docker 容器。

## 📋 事前準備

- 已安裝 [Docker](https://docs.docker.com/get-docker/)。
- 已安裝 [Docker Compose](https://docs.docker.com/compose/install/) (通常未包含在 Docker Desktop/Plugin 中)。

## 🛠️ 安裝教學

1. **複製專案**:

   ```bash
   git clone https://github.com/Wester-Liou/bandwidth-vending.git
   cd bandwidth-vending
   ```

2. **設定環境變數**:
   複製範例設定檔：

   ```bash
   cp .env.example .env
   ```

3. **編輯 `.env`**:
   開啟 `.env` 並填入各服務的帳號資訊 (Email, 密碼, Token)。

   ```ini
   # 裝置名稱 (將顯示在儀表板上)
   DEVICE_NAME=bandwidth-vending

   # Honeygain
   HONEYGAIN_EMAIL=your_email@example.com
   HONEYGAIN_PASSWORD=your_password

   # PacketStream
   PS_CLIENT_CID=your_cid

   # Pawns.app
   PAWS_EMAIL=your_email@example.com
   PAWS_PASSWORD=your_password

   # TraffMonetizer
   TRAFFMONETIZER_TOKEN=your_token
   ```

## ▶️ 使用說明

### 啟動服務

在背景執行容器：

```bash
docker-compose up -d
```

### 查看日誌

查看容器運行狀態：

```bash
docker-compose logs -f
```

### 停止服務

停止並移除容器：

```bash
docker-compose down
```

## ⚙️ 設定詳情

請參閱 `.env` 查看所有可設定選項。請確保您的憑證安全，切勿將實際的 `.env` 檔案提交到版本控制系統 (預設已被忽略)。

## 🔄 自動更新

本設定包含 **Watchtower**，它將每小時自動檢查並更新您的容器至最新映像檔。
