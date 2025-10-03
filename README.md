# ReceiptMind — AI Receipt Scanner (React + GCP + Gemini)

Upload a receipt image, sign in securely, and get structured results (merchant, date, totals, line items, tax, categories, duplicate check).
Built for portfolio signal: React + Docker + Firebase Auth + Firestore/Storage + Vertex AI Gemini on Cloud Run.

<!-- Badges -->
![React](https://img.shields.io/badge/React-18-blue)
![Node](https://img.shields.io/badge/Node-20-green)
![Docker](https://img.shields.io/badge/Docker-Containerized-informational)
![GCP](https://img.shields.io/badge/GCP-Cloud%20Run%20%7C%20Firestore%20%7C%20Storage-orange)
![Vertex AI](https://img.shields.io/badge/Vertex%20AI-Gemini%201.5%20Flash-purple)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

## ✨ Features
- Email/Google sign-in via Firebase Authentication
- Image upload to Cloud Storage (signed URL flow)
- AI parsing with Google Gemini (multimodal vision + reasoning)
- Structured output to Firestore (line items, totals, confidence)
- Clean React UI with results history, loading/error states
- Fully Dockerized; deployable on Cloud Run
