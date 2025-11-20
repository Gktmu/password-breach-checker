Password Breach Checker & Strong Password Generator

A web-based tool that allows users to check whether a password has been exposed in known data breaches and also generate strong, secure passwords.
It uses SHA-1 hashing + HaveIBeenPwned (HIBP) API (k-anonymity model) for breach checking and zxcvbn for strength estimation.

🚀 Features
🔐 Password Breach Checker

Checks if a password has been compromised in known leaks.

Uses client-side hashing (SHA-1) for privacy — password never leaves the browser.

Sends only first 5 characters of hash to HIBP API (k-anonymity protocol).

Displays:

Breach Status (Compromised / Safe)

Number of times found in breaches

Strength score (0–4) using zxcvbn.

🔑 Strong Password Generator

Generates secure passwords using customizable settings:

Lowercase (a–z)

Uppercase (A–Z)

Digits (0–9)

Symbols (!@#$...)

User-controlled password length.

One-click Generate and Copy buttons.

🖼️ Interface Preview

(Add your screenshot here)
Example:

assets/screenshot.png

🧠 How Password Breach Checking Works

User enters password.

Password is hashed in browser using SHA-1.

Only the first 5 characters of the hash (prefix) are sent to HIBP API.

API returns a list of matching hash suffixes.

App compares locally → detects if password is breached.

Shows status + password strength score.

This ensures complete privacy — your password is never uploaded.

🛠️ Technologies Used
Frontend

HTML5, CSS3

Vanilla JavaScript

Libraries / APIs

zxcvbn (password strength estimation)

HaveIBeenPwned API

SHA-1 hashing

📦 Project Structure
/project-folder
│── index.html
│── style.css
│── script.js
│── README.md
│── assets/
│     └── screenshot.png

📥 Setup & Usage
🔧 Run Locally

Clone the repository:

git clone https://github.com/yourusername/password-breach-checker.git


Open the index.html file in your browser.

No backend required — everything works client-side.

🔐 Privacy & Security

Passwords are never stored, logged, or sent to any server.

SHA-1 hashing occurs locally in the browser.

Uses HaveIBeenPwned’s k-anonymity model for safe breach lookup.

This project is designed for educational and personal security awareness, not for handling real user credentials.

📄 Data Flow Diagram (DFD)
User → Inputs Password
       → Browser hashes with SHA-1
       → Sends first 5 chars of hash prefix to HIBP
HIBP API → Returns matching hash suffixes
Browser → Compares + Displays result
User → Generates new strong password (optional)

📘 Future Enhancements

Dark mode UI

Save password history locally

QR export for mobile use

Desktop app (Electron) version

🤝 Contributions

Pull requests are welcome. For major changes, please open an issue first to discuss.

📜 License

This project is open-source under the MIT License.
