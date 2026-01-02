# LOGIHUB-driver-checkin-system
LOGIHUB is a logistics hackathon project featuring a smart driver check-in system with GPS-based location capture, multilingual UI, QR-ready access, and Google Sheets–powered backend logging.

🚚 Driver Check-In Module | LOGIHUB
The Driver Check-In System is a mobile-optimized web solution designed to streamline logistics operations. It bridges the gap between physical arrival and digital logging by ensuring high-integrity data collection through automated GPS verification and a multilingual interface.

🌟 Key Features
📱 Optimized Driver Experience
Mobile-First Design: A sleek, dark-themed UI built for quick interaction in high-pressure logistics environments.

Multi-Screen Flow: Logical progression from Start → Language Selection → Trip Details.

QR-Ready: Optimized for instant access via QR codes posted at hub entrances.

🌍 Multilingual Support
To accommodate a diverse workforce, the module features dynamic, JSON-based translation switching:

Supported Languages: English, Hindi (हिंदी), Bengali (বাংলা), Tamil (தமிழ்), and Telugu (తెలుగు).

Note: Language selection adjusts the UI for user comfort without altering backend data consistency.

📍 Intelligent Location Verification
Zero-Trust Reporting: Uses the Browser Geolocation API combined with Google Maps Reverse Geocoding to auto-fill the current location.

⚙️ How It Works
Authentication & Entry: Driver scans a QR code at the station.

Geolocation: The app requests GPS permissions and fetches the human-readable address.

Submission: Driver enters Truck ID, Name, and Station.

Data Logging: The backend securely transmits the payload to a centralized Google Sheet for real-time monitoring.

📊 Data Schema
Every submission captures:

Timestamp | Current Location (GPS) | Station (Manual) | Truck Number | Driver ID/Name | Route (From/To)

💡 Why This Matters
Accuracy: Eliminates "buddy punching" or incorrect station reporting.

Efficiency: Reduces check-in time from minutes to seconds.

Scalability: Provides a structured dataset ready for future predictive analytics and bottleneck identification.

Anti-Tamper Logic: The GPS-derived location field is locked, preventing manual overrides.

Verification Loop: Drivers manually enter the "Station Name," allowing the backend to flag discrepancies if Current_Location ≠ Station.
