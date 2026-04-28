# 🛡️ SentinelAI: Secure Agentic AI Governance Gateway

**SentinelAI** is a proactive AI-governance middleware designed to mitigate the risks of accidental data breaches in corporate environments. Built with a robust **Laravel** and **React** architecture, it acts as a secure "middleman" that intercepts, analyzes, and secures real-time interactions between employees and Large Language Models (LLMs).

In an era where **76% of knowledge workers** in the Philippines are adopting AI tools, SentinelAI provides the necessary oversight to prevent the unauthorized sharing of Personally Identifiable Information (PII) and sensitive institutional data—addressing the same vulnerabilities that led to high-profile leaks at companies like Samsung.

---

## 🚀 Key Features

### 🔍 Risk Mitigation & Governance
- **Auto-Masking Engine:** Real-time detection and redaction of PII (names, emails, etc.) before data reaches external AI providers.
- **Agentic Interception:** Orchestrated via **n8n**, the system evaluates the intent and content of every prompt against organizational security policies.
- **Heartbeat Monitoring:** Custom middleware tracks "Active" status and session health, ensuring oversight of all AI-integrated workflows.

### 📊 Admin Command Center
- **Risk-Level Analytics:** Detailed dashboards displaying violation history and frequency of sensitive data triggers.
- **Policy Deployment:** Instantly push new organizational rules to the gateway without redeploying code.
- **Audit Logs:** Complete transparency into how AI is being utilized within the organization.

### 🔐 Secure Interface
- **Hardened Chat UI:** A dedicated, secured interface for employees that forces compliance protocols natively.
- **Firebase Authentication:** Secure Google Sign-In and session management for granular access control.

---

## 🛠️ Technical Architecture

| Category        | Technology                                      |
|----------------|-------------------------------------------------|
| **Frontend**   | React, Tailwind CSS, Shadcn/UI                  |
| **Backend**    | Laravel (PHP), MySQL                            |
| **Identity**   | Firebase Authentication                         |
| **Data Layer** | Firebase Firestore (Hybrid Real-time Management)|
| **Automation** | n8n (Containerized via Docker)                  |
| **Intelligence** | Gemini AI (Google AI Studio)                 |
| **Geospatial** | Nominatim API (Coordinates to Text translation) |

---

## 🔄 System Logic Flow (ISC)

1. **Ingestion:** User prompt is captured by the React frontend.  
2. **Middleware:** Laravel backend wraps the payload in JSON and forwards it to n8n.  
3. **Governance:**  
   - n8n Agent receives JSON  
   - Transforms to Text  
   - AI Agent evaluates risk  
   - Transforms back to JSON  
4. **Response:** Masked and secured data is returned to the user through the Laravel gateway.

---

## 📦 Project Structure

```bash
Sentinel-AI/
├── Front-End/         # React + Tailwind CSS client
├── Back-End/          # Laravel API + Governance Logic
├── Docker/            # Containerization for n8n workflows
└── README.md          # Project Documentation
```

---

## ⚙️ Installation & Setup

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/Sentinel-AI.git
cd Sentinel-AI
```

### 2. Back-End Setup
```bash
cd Back-End
composer install
cp .env.example .env   # Configure your MySQL and Firebase keys
php artisan migrate
php artisan serve
```

### 3. Front-End Setup
```bash
cd ../Front-End
npm install
npm run dev
```

### 4. n8n Setup
Ensure Docker is running and execute:

```bash
docker run -it --rm --name n8n -p 5678:5678 n8nio/n8n
```

---

## 📜 Compliance & Safety

This system is built to align with the Philippine Data Privacy Act (DPA) and the National Privacy Commission (NPC) guidelines regarding AI data processing. By implementing an internal governance layer, organizations can leverage Agentic AI while maintaining strict "Privacy Maturity" standards.

---

## 👨‍💻 Author

**Marck Anthony Sabado**  
Incoming Senior BSIT Student | Lead Developer | AI Researcher
