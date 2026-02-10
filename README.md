🎬 SyncWatch – Real-Time Video Streaming & Sync Platform

A production-grade, free-tier friendly Watch Party application that lets users upload videos, stream them efficiently, and watch together in perfect sync — with real-time chat and playback control.

This project is designed with scalability, reliability, and cost-efficiency in mind, using modern web technologies and industry-standard streaming techniques.

🚀 What This Project Does

Host creates a room (Meet ID)

Friends join using a link or code

Host uploads a video chunk-by-chunk

Video is converted to HLS (HTTP Live Streaming)

Everyone watches the video in sync

Real-time chat, play, pause, seek, and presence

Fully deployable using 100% free-tier services

This is not a screen-sharing solution — it’s a true streaming system built the right way.

🧠 Key Engineering Highlights
✅ Chunked Video Upload

Uploads large videos safely (100MB+)

Resume-friendly

No request timeouts

Free-tier optimized

✅ HLS Streaming (Lag-Free)

Video converted into .m3u8 + .ts segments

Adaptive, low-bandwidth streaming

Works smoothly over long distances

✅ Real-Time Synchronization

Socket.IO ensures:

Play / Pause / Seek sync

Chat messaging

User join / leave presence

Host-controlled playback for perfect alignment

✅ Free-Tier Optimized Architecture

No AWS egress surprises

Designed to run entirely on free plans

Smart limits to protect resources

🏗️ Tech Stack
Frontend

React + Vite

Tailwind CSS (dark, minimal UI)

HLS.js / Video.js

Socket.IO Client

Axios

Backend

Node.js + Express

Socket.IO

FFmpeg (video → HLS conversion)

In-memory room management

Storage & Streaming

Cloudflare R2 (10GB free, zero egress cost)

HLS-ready object storage

Hosting (Free Tier)

Frontend → Vercel / Netlify

Backend → Render / Fly.io

Storage → Cloudflare R2

🧩 System Architecture
Frontend (React)
│
├── REST API (Express)
│   ├── Room Creation
│   ├── Chunk Upload
│   ├── Video Processing
│
├── Socket.IO
│   ├── Chat
│   ├── Playback Sync
│   └── User Presence
│
└── HLS Video Player
    └── Streams from Cloudflare R2

🔑 Core Features

🎥 Chunk-by-chunk video upload

📺 HLS-based streaming

🔄 Play / Pause / Seek synchronization

💬 Real-time chat

👥 User presence tracking

🔗 Short Meet ID room system

🌙 Clean, dark UI

📱 Responsive layout

⚙️ API Overview

POST /api/room/create → Create room

POST /api/room/join → Join room

POST /api/upload/chunk → Upload video chunk

POST /api/upload/complete → Merge & convert

GET /api/video/:roomId → Get HLS stream URL

🧪 Testing

Fully testable using Postman

Chunk uploads supported in Postman

Multiple browser tabs for Socket.IO testing
