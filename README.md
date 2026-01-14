# Personal Website Source Code

<p align="center">
  <img src="https://img.shields.io/badge/Build-Passing-brightgreen" alt="Build Status">
  <a href="https://developer.mozilla.org/en-US/docs/Web/HTML"><img src="https://img.shields.io/badge/Stack-HTML5%20%2F%20ES6-orange" alt="Tech Stack"></a>
  <a href="https://supabase.com"><img src="https://img.shields.io/badge/Backend-Supabase-green" alt="Supabase"></a>
  <a href="https://www.jsdelivr.com"><img src="https://img.shields.io/badge/Network-jsDelivr%20CDN-red" alt="CDN"></a>
</p>

## 📖 Introduction

This repository contains the source code for a lightweight, static personal website and portfolio. 

The project implements a **Serverless Architecture**, utilizing **Supabase** as a headless CMS for metadata management and **GitHub** as an object storage solution for static assets. This design eliminates the need for traditional server maintenance while ensuring high performance and low latency via global CDN.

## 🚀 Key Features

- **Decoupled Architecture**: 
  - Source code resides in the `main` branch.
  - Binary assets (images/media) are isolated in the `assets` orphan branch to optimize git history size.
- **Dynamic Content Loading**: Fetches real-time data (Titles, Descriptions, Links) from a remote PostgreSQL database (Supabase).
- **Custom Lightbox**: A built-in, dependency-free modal for high-resolution media viewing.
- **Secure Admin Panel**: 
  - A mobile-responsive web dashboard for content management.
  - Implements **Client-side AES Encryption** to protect API credentials, ensuring security even in a static hosting environment.
- **CDN Integration**: Assets are automatically delivered via jsDelivr for optimal load speeds.

## 🛠️ Technical Stack

| Component | Technology | Description |
| :--- | :--- | :--- |
| **Frontend** | Vanilla JS / CSS3 | No heavy frameworks, purely native performance. |
| **Database** | Supabase | Stores metadata mapping for the gallery. |
| **Storage** | Git File System | Version-controlled asset storage via `assets` branch. |
| **Security** | Crypto-JS | Handles secure token decryption on the client side. |

## 📂 Repository Structure

```text
├── index.html          # Main entry point
├── gallery.html        # Dynamic media grid
├── admin_panel.html    # Secure upload terminal (Restricted access)
├── config.json         # Encrypted configuration file
├── README.md           # Documentation
└── assets/             # (Located in a separate branch)
📦 Deployment
This project is designed to be deployed on any static site hosting provider:
GitHub Pages
Vercel
Netlify
Cloudflare Pages
🔧 Setup Guide
Clone the repository.
Configure your Supabase URL and Anon Key in the script tags.
Generate an encrypted configuration file using CryptoJS for the admin panel.
Push the code to the main branch.
Create an orphan assets branch for media storage.
📄 License
This project is open-source and available under the MIT License.
