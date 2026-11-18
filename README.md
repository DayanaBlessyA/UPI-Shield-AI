# 🛡️ UPI Shield AI

**An AI-assisted digital payment safety screening tool for suspicious UPI messages and payment screenshots.**

UPI Shield AI helps users identify potential warning signs in suspicious payment-related messages and screenshots. It provides a risk score, explains detected indicators, and recommends safer actions.

## ✨ Features

- **Message Scanner:** Screens SMS, WhatsApp messages, and UPI payment requests.
- **Screenshot Scanner:** Uses Gemini multimodal analysis to review uploaded payment screenshots.
- **Risk Assessment:** Displays a risk score from 0–100 with Low, Medium, or High classification.
- **Warning Indicators:** Explains suspicious patterns and potential fraud signals.
- **Safety Recommendations:** Provides practical steps to avoid common UPI scams.
- **Analysis History:** Stores recent analysis results locally using SQLite.
- **Demo Scenarios:** Includes sample messages for testing.

## 🧠 AI Models and APIs Used

### Google Gemini API

The application integrates the Google Gemini Developer API through its REST `generateContent` endpoint.

The following model IDs are configured in the application, in fallback order:

- `gemini-4-hydrogen`
- `gemini-3.5-flash-lite`
- `gemini-3.8-flash`

Gemini is used for AI-assisted text and image analysis. Actual model availability depends on API access and service availability.

### Local Rule-Based Screening

Python regular expressions identify common warning patterns, including:
- Urgent account-blocking threats
- Suspicious links
- OTP and UPI PIN requests
- Fake prize and refund offers
- Misleading UPI collect requests

## 🛠️ Technology Stack

- Python
- Streamlit
- Google Gemini Developer API
- Requests
- Pillow (PIL)
- SQLite

## 🚀 How to Run Locally

### 1. Clone the repository

```bash
git clone https://github.com/DayanaBlessyA/UPI-Shield-AI.git
cd UPI-Shield-AI
```

### 2. Install dependencies

```bash
python -m pip install -r requirements.txt
```

### 3. Start the application

```bash
python -m streamlit run app.py
```

### 4. Configure Gemini API

- Open the application in your browser.
- Obtain an API key from [Google AI Studio](https://aistudio.google.com/app/apikey).
- Paste the key into the Gemini API field in the main dashboard.
- Use the message and screenshot scanners.

Message screening can also use local rule-based checks without an API key. Screenshot analysis requires Gemini API access.

## 🎥 Demo Video

YouTube demo link: **To be added after video upload.**

## ⚠️ Important Limitations

UPI Shield AI is a student-built hackathon prototype, not a bank-integrated fraud detection service.

- Risk scores are screening indicators, not proof of fraud or safety.
- The application does not verify bank accounts, UPI IDs, QR destinations, or transactions.
- It does not initiate payments.
- Never enter real UPI PINs, OTPs, passwords, PAN numbers, or other sensitive information.

## 📦 Project Repository

[UPI Shield AI – GitHub](https://github.com/DayanaBlessyA/UPI-Shield-AI)

## 🙌 Credits

- Streamlit
- Google Gemini API
- Python
- Requests
- Pillow
