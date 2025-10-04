# ReceiptMind — AI Receipt Scanner (React + GCP + Gemini)

Upload a receipt image, sign in securely, and get structured results (merchant, date, totals, line items, tax, categories, duplicate check).
Built for portfolio signal: React + Docker + Firebase Auth + Firestore/Storage + Vertex AI Gemini on Cloud Run.

<!-- Badges -->
![React](https://img.shields.io/badge/React-18-blue)
![Node](https://img.shields.io/badge/Node-20-green)
![Docker](https://img.shields.io/badge/Docker-Containerized-informational)
![GCP](https://img.shields.io/badge/GCP-Cloud%20Run%20%7C%20Firestore%20%7C%20Storage-orange)
![Vertex AI](https://img.shields.io/badge/Vertex%20AI-Gemini%201.5%20Flash-purple)

## ✨ Features
- Email/Google sign-in via Firebase Authentication
- Image upload to Cloud Storage (signed URL flow)
- AI parsing with Google Gemini (multimodal vision + reasoning)
- Structured output to Firestore (line items, totals, confidence)
- Clean React UI with results history, loading/error states
- Fully Dockerized; deployable on Cloud Run

## 📦 Tech Stack
- **Frontend**: React, TypeScript, Fetch API
- **Backend**: Node 20 + Express
- **Auth**: Firebase Authentication
- **Data**: Firestore (Native)
- **Storage**: Cloud Storage
- **AI**: Vertex AI — Gemini 1.5 Flash
- **Infra**: Docker, Cloud Run, Artifact Registry, Secret Manager

## 🔐 Data Models (Firestore)
- `users/{uid}`
  - `userId`: int/pk
  - `username`: string
  - `createdAt`: timestamp
- `receipts/{receiptId}`
  - `userId`: int/pk
  - `createdAt`: timestamp
  - `imagePath`: string
  - `merchant`: string
  - `purchaseDate`: string|timestamp
  - `subtotal`: number
  - `tax`: number
  - `total`: number
  - `currency`: string
  - `lineItems`: Array<{ description, qty, unitPrice, amount, category}>
  - `modelMeta`: { model: "gemini-1.5-flash", promptVersion: "v1" }

<!-- ## 🚀 Quick Start (without Docker)
1. **Frontend**
   ```bash
   cd apps/web
   npm install
   npm run dev

2. **Backend**
   cd apps/api
   npm install
   npm run dev -->
