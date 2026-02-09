# BlesProduction Portfolio + AI Chatbot (Vercel)

## 1) Deploy to Vercel
1. Push folder ini ke GitHub (atau upload langsung ke Vercel).
2. Di Vercel: **New Project** → pilih repo → Deploy.

## 2) Set Environment Variables (wajib)
Vercel → Project → **Settings** → **Environment Variables**
- `OPENAI_API_KEY` = API key OpenAI kamu
- `OPENAI_MODEL` (opsional) = default `gpt-5`

Lalu redeploy.

## 3) Cara kerja
- Frontend (index.html) memanggil endpoint serverless: `POST /api/chat`
- Endpoint itu memanggil OpenAI Responses API: `POST https://api.openai.com/v1/responses`
- API key hanya ada di server (Vercel), aman.

## 4) Catatan
- Chat menyimpan konteks pendek di browser (in-memory). Reload halaman = konteks hilang.
- Kalau kamu mau streaming token (teks muncul sambil jalan), bilang ya — aku bisa upgrade ke mode streaming.
