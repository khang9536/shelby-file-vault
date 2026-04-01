# 🗄️ Shelby File Vault

Ứng dụng upload & quản lý file trên **Shelby Protocol** (Aptos Testnet).

---

## ✅ Yêu cầu trước khi bắt đầu

1. Cài **Node.js** (v18 trở lên): https://nodejs.org
2. Cài extension **Petra Wallet** trên Chrome: https://petra.app
3. Trong Petra: chuyển sang **Aptos Testnet**

---

## 🚀 Cách chạy app (từng bước)

### Bước 1 — Cài dependencies

Mở Terminal (hoặc Command Prompt), vào thư mục dự án:

```bash
cd shelby-file-vault
npm install
```

### Bước 2 — Tạo file `.env`

Copy file `.env.example` thành `.env`:

```bash
cp .env.example .env
```

Sau đó điền API keys vào file `.env`:

- **VITE_APTOS_API_KEY**: Lấy miễn phí tại https://developers.aptoslabs.com
- **VITE_SHELBY_API_KEY**: Lấy sau khi được approve Early Access tại https://developers.shelby.xyz

### Bước 3 — Chạy app

```bash
npm run dev
```

Mở trình duyệt: **http://localhost:5173**

---

## 💰 Chuẩn bị token Testnet

Để upload file, bạn cần 2 loại token testnet (miễn phí):

| Token | Dùng để | Lấy ở đâu |
|-------|---------|-----------|
| APT (testnet) | Trả phí gas | https://aptos.dev/network/faucet |
| ShelbyUSD | Trả phí upload (1/lần) | Discord Shelby: https://discord.gg/shelbyserves |

---

## 📱 Cách dùng app

1. Mở app → Click **"Kết nối ví"** → Chọn Petra
2. Kéo thả file vào ô upload (hoặc click để chọn)
3. Xác nhận transaction trong Petra Wallet
4. File sẽ xuất hiện trong danh sách bên dưới
5. Click **"↓ Tải xuống"** hoặc **"🔗"** để copy link trực tiếp

---

## 🏗️ Cấu trúc dự án

```
shelby-file-vault/
├── src/
│   ├── App.tsx                 # Component chính
│   ├── index.css               # Styles toàn cục
│   ├── main.tsx                # Entry point
│   ├── components/
│   │   ├── Header.tsx          # Header + kết nối ví
│   │   ├── FileUpload.tsx      # Upload file lên Shelby
│   │   ├── FileList.tsx        # Danh sách file đã upload
│   │   └── WalletProvider.tsx  # Aptos wallet context
│   └── lib/
│       └── shelby.ts           # Shelby + Aptos client
├── .env.example
└── package.json
```

---

## 🛠️ Tech stack

- **React + TypeScript + Vite**
- **@shelby-protocol/sdk** — Shelby storage SDK
- **@aptos-labs/ts-sdk** — Aptos blockchain client
- **@aptos-labs/wallet-adapter-react** — Wallet connection

---

Built with ❤️ on Shelby Protocol Early Access
