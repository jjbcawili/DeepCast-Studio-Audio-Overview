# DeepCast Studio — Audio Overview

This repository contains the **DeepCast Studio Audio Overview** application source snapshot: a two-host AI podcast generator built around **Jiro** and **Sharpay** for entertainment, music-industry, pop-culture, and deep-dive conversations.

## Live DeepCast Studio application

**Current ChatGPT Site:** https://deepcast-studio.jjbcawili.chatgpt.site

> **Repository sync status:** The live ChatGPT Site and this GitHub repository are separate deployment surfaces. This repository currently contains the latest source snapshot committed here; do not treat it as byte-for-byte identical to the live site unless a fresh source export has been compared and synchronized.

## What this source snapshot includes

- React 19 + TypeScript frontend
- Vite development/build tooling
- Express server
- Google Gemini outline and script generation
- ElevenLabs two-host audio generation
- `eleven_v3` Text-to-Dialogue primary model
- `eleven_multilingual_v2` fallback
- Deterministic generation seeds
- Default hosts: Jiro and Sharpay

## Run locally

### Prerequisites

- Node.js 20 or newer
- Gemini API key
- ElevenLabs API key

### Setup

```bash
npm install
cp .env.example .env.local
npm run dev
```

The development server normally runs at `http://localhost:3000` unless `PORT` is overridden.

## Environment variables

| Variable | Required | Purpose |
| --- | --- | --- |
| `GEMINI_API_KEY` | Yes | Generates episode outlines and scripts. |
| `ELEVENLABS_API_KEY` | Yes | Generates voice previews and podcast dialogue audio. |
| `JIRO_ELEVENLABS_VOICE_ID` | No | Overrides Jiro's default ElevenLabs voice. |
| `SHARPAY_ELEVENLABS_VOICE_ID` | No | Overrides Sharpay's default ElevenLabs voice. |
| `APP_URL` | No | Public application URL for integrations or callbacks. |
| `PORT` | No | Server port. Defaults to `3000`. |

Never commit real API keys, tokens, OAuth secrets, or production credentials.

## Commands

```bash
npm run dev
npm run lint
npm run build
npm start
npm run clean
```

## Project boundary

This repository belongs to the **DeepCast Studio application**. The separate **Taylor Swift Deep Dive — Audio Overview Project** remains a distinct project unless an explicit cross-project change is approved.
