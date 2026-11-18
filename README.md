# UPI Shield AI

An AI-assisted prototype for screening suspicious UPI/payment messages and screenshots.

## Features
- Text-message screening with local warning-pattern checks.
- Optional Gemini API analysis for richer explanations.
- Optional Gemini vision analysis for uploaded screenshots.
- Risk score, warning indicators, safety recommendations.
- SQLite history.
- Demo scenarios for quick evaluation.

## Run locally
1. Install Python 3.10 or newer.
2. Open a terminal in this folder.
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Start the app:
   ```bash
   streamlit run app.py
   ```

## Gemini API (optional)
Run the app and paste your Gemini API key into the sidebar. The key is used only in the current app session and is not written to the database. Without a key, local text screening still works. Screenshot analysis requires Gemini vision access.

## Important limitations
This is a hackathon screening prototype, not a bank-integrated fraud detection service. A risk score is an indicator, not proof that a message or payment is fraudulent or safe. It does not verify UPI IDs, QR destinations, accounts, or transactions, and it never initiates payments. Never enter real UPI PINs, OTPs, passwords, or other credentials.

## Credits
- Streamlit
- Requests
- Pillow
- Google Gemini API (optional)
