# 🛡️ AIPatrol — AI Data Leak Prevention

> Stop sensitive data reaching AI tools before it's too late.

AIPatrol is a lightweight browser extension that warns you before API keys, passwords, PII, and confidential data are submitted to AI tools like ChatGPT, Claude, Gemini, Perplexity, and more.

![Version](https://img.shields.io/badge/version-1.0.0-blue)
![License](https://img.shields.io/badge/license-BSL_1.1-blue)
![Manifest](https://img.shields.io/badge/manifest-v3-orange)

---

## ✨ Features

- 🔍 **Real-time detection** — scans text as you type or paste
- 🚨 **Warn before send** — intercepts Enter key, button clicks, and paste events
- 🏷️ **Severity levels** — CRITICAL / HIGH / MEDIUM / LOW with colour-coded badges
- 📋 **28+ detection rules** — API keys, passwords, SSNs, passports, IBANs, tax IDs, SSH keys, internal IPs, confidential documents and more
- ⚙️ **JSON-driven rules** — add or customise rules without touching code
- 🔒 **100% local** — no data ever leaves your device
- 📦 **26KB** — tiny footprint, no trackers, no analytics

---

## 🌐 Supported AI Tools

| Platform | Supported |
|---|---|
| ChatGPT (chatgpt.com) | ✅ |
| Claude (claude.ai) | ✅ |
| Gemini (gemini.google.com) | ✅ |
| Perplexity (perplexity.ai) | ✅ |
| Microsoft Copilot | ✅ Chrome only* |
| Google Search | ✅ |
| Bing | ✅ |
| Poe | ✅ |
| You.com | ✅ |

> *Microsoft Edge blocks third-party extensions on `copilot.microsoft.com` at the browser level. Use Chrome for Copilot coverage.

---

## 🚀 Installation

### From the Store (recommended)
- [Chrome Web Store](#) *(coming soon)*
- [Microsoft Edge Add-ons](#) *(coming soon)*

### Load unpacked (development)
```bash
git clone https://github.com/ashoksudhakar2001-svg/aipatrol.git
cd aipatrol
npm install
node build.mjs
```
Then in Chrome/Edge:
1. Go to `chrome://extensions` (or `edge://extensions`)
2. Enable **Developer mode**
3. Click **Load unpacked** → select the `dist/` folder

---

## 🏷️ Risk Levels

| Level | Colour | Examples |
|---|---|---|
| **CRITICAL** | 🔴 Red | API keys, private keys, SSNs, passwords |
| **HIGH** | 🟠 Orange | Passports, IBANs, auth tokens, tax IDs |
| **MEDIUM** | 🟡 Yellow | IP addresses, phone numbers, addresses |
| **LOW** | 🟢 Green | Confidential keywords (need other signals) |

---

## ⚙️ Adding Custom Rules

Edit [`src/detection/rules.json`](src/detection/rules.json) — no coding required:

```json
{
  "id": "my_custom_rule",
  "description": "My secret project codename",
  "pattern": "PROJECT-X|CODENAME-ALPHA",
  "flags": "gi",
  "severity": "high",
  "action": "warn"
}
```

Rebuild with `node build.mjs` and reload the extension.

---

## 🔒 Privacy

AIPatrol processes everything locally in your browser. No data is ever transmitted.

📄 [Full Privacy Policy](https://ashoksudhakar2001-svg.github.io/aipatrol/privacy.html)

---

## 📄 License

This project is licensed under the **[Business Source License 1.1](LICENSE)**.

- ✅ Free for personal, non-commercial use
- ✅ Source code visible for security auditing
- ❌ Commercial use requires a licence — contact [ashok.sudhakar2001@gmail.com](mailto:ashok.sudhakar2001@gmail.com)
- 🔄 Converts to Apache 2.0 on 2029-05-25

© 2025 Sudhakar Ethirajulu
