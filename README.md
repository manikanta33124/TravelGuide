# 🌍 TravellingGuide

> An AI-powered full-stack travel guide application that helps users explore destinations and generate personalized audio travel guides.

## 🚀 Live Demo

**[🚀 Live Demo: TravellingGuide](https://travellguider.netlify.app)**

## 💻 GitHub Repository

[📂 View TravellingGuide on GitHub](https://github.com/manikanta33124/TravelGuide)

---

## 📌 Project Overview

**TravellingGuide** is a full-stack web application designed to make travel exploration more informative and engaging.

The application allows users to select a travel destination and provide preferences such as language and voice options. It uses a Python Flask backend to process requests and integrates external AI services to generate travel-related content and convert the generated information into audio.

The project demonstrates how a frontend application can communicate with a backend API and integrate third-party AI services to provide an interactive travel experience.

### 🎯 Problem It Solves

Travelers often need to search through multiple sources to find useful information about a destination. TravellingGuide aims to provide travel information through a simple interface and make the experience more convenient by providing an **audio-based travel guide**.

---

## ✨ Features

- 🗺️ **Destination Exploration** – Enter and explore travel destinations.
- 🤖 **AI-Generated Travel Information** – Uses the Gemini API to generate travel-related content.
- 🌐 **Language Selection** – Allows users to select their preferred language for the generated guide.
- 🎙️ **Voice Selection** – Provides voice options for generating the audio guide.
- 🔊 **Audio Guide Generation** – Uses the Murf API to convert generated travel information into audio.
- 🎧 **Audio Playback** – Allows users to listen to the generated travel guide.
- 📱 **Responsive User Interface** – Designed to provide a user-friendly experience across different screen sizes.
- 🔗 **Frontend–Backend Integration** – Communicates with a Flask REST API for processing requests.
- 🔐 **Environment Variable Support** – API credentials are managed through environment variables rather than being hardcoded into the application.

---

## 🛠️ Technologies Used

### 🎨 Frontend

- HTML5
- CSS3
- JavaScript
- Fetch API

### ⚙️ Backend

- Python
- Flask
- Flask-CORS
- Gunicorn

### 🤖 APIs & Libraries

- **Google Gemini API** – Used to generate travel-related content.
- **Murf API** – Used for text-to-speech/audio generation.
- `python-dotenv` – Used to load environment variables securely.
- `requests` – Used for making HTTP requests from the backend.

### ☁️ Deployment

- **GitHub** – Source code management
- **Render** – Backend deployment
- **Netlify** – Frontend deployment

---

## 📂 Project Structure

```text
TravellingGuide/
│
├── Backend/
│   ├── app.py
│   ├── requirements.txt
│   └── .env
│
└── Frontend/
    ├── index.html
    └── index.js
```

> ⚠️ `.env` is used only for local configuration and should **not** be committed to GitHub.

---

## ⚙️ Installation and Setup

### 1. Clone the Repository

```bash
git clone https://github.com/manikanta33124/TravelGuide.git
```

Navigate into the project:

```bash
cd TravelGuide
```

---

### 2. Set Up the Backend

Navigate to the backend directory:

```bash
cd Backend
```

Create a Python virtual environment:

```bash
python -m venv .venv
```

Activate the virtual environment on Windows:

```powershell
.venv\Scripts\activate
```

Install the required dependencies:

```bash
pip install -r requirements.txt
```

---

## 🔐 Environment Variables

Create a `.env` file inside the `Backend` directory:

```text
Backend/
├── app.py
├── requirements.txt
└── .env
```

Add your API credentials to `.env`:

```env
GEMINI_API_KEY=your_gemini_api_key_here
MURF_API_KEY=your_murf_api_key_here
```

### 🔒 Security Note

Never commit the `.env` file to GitHub.

Add the following to `.gitignore`:

```gitignore
.env
Backend/.env
__pycache__/
*.pyc
.venv/
venv/
```

**Never expose API keys, passwords, tokens, or other credentials in source code or public repositories.**

---

## ▶️ How to Run

### Backend

From the `Backend` directory:

```bash
python app.py
```

The Flask backend will run locally at:

```text
http://127.0.0.1:5000
```

The main API endpoint is:

```text
/generate-audio-guide
```

---

### Frontend

The frontend is a static HTML/JavaScript application.

You can run it using the **Live Server** extension in VS Code:

1. Open `Frontend/index.html`.
2. Right-click the file.
3. Select **Open with Live Server**.
4. The application will open in your browser.

Make sure the frontend API URL points to the appropriate backend URL.

For local development:

```javascript
const GENERATE_AUDIO_GUIDE_API_URL =
    "http://127.0.0.1:5000/generate-audio-guide";
```

For the deployed application, it should point to the deployed Render backend:

```javascript
const GENERATE_AUDIO_GUIDE_API_URL =
    "https://your-render-backend-url.onrender.com/generate-audio-guide";
```

---

## ☁️ Deployment

The application is deployed using separate hosting services for the frontend and backend.

### Frontend

The frontend is deployed on **Netlify**:

🚀 **[TravellingGuide Live Application](https://travellguider.netlify.app)**

### Backend

The Flask backend is deployed on **Render**.

The backend uses environment variables configured in Render for the Gemini and Murf API credentials.

### Deployment Architecture

```text
                    👤 User
                      │
                      ▼
             ┌─────────────────┐
             │     Netlify     │
             │    Frontend     │
             │ HTML/CSS/JS     │
             └────────┬────────┘
                      │
                      │ API Request
                      ▼
             ┌─────────────────┐
             │     Render      │
             │ Python + Flask  │
             └────────┬────────┘
                      │
              ┌───────┴────────┐
              ▼                ▼
        🤖 Gemini API      🔊 Murf API
              │                │
              └───────┬────────┘
                      ▼
                 Travel Guide
```

---

## 📸 Screenshots

Screenshots of the application can be added here.

### 🏠 Home / Travel Guide

_Add screenshot here_

```text
![TravellingGuide Home](screenshots/home.png)
```

### 🗺️ Destination Selection

_Add screenshot here_

```text
![Destination Selection](screenshots/destination.png)
```

### 🎧 Generated Audio Guide

_Add screenshot here_

```text
![Audio Guide](screenshots/audio-guide.png)
```

> Create a `screenshots` folder in the repository and replace the placeholders with your actual screenshots.

---

## 🔮 Future Enhancements

The following are potential improvements for future versions:

- 🗺️ Add interactive maps and destination locations.
- 🌦️ Integrate real-time weather information.
- 🏨 Add hotel and accommodation recommendations.
- 🍽️ Add restaurant and local food recommendations.
- 📍 Provide personalized travel itineraries.
- 👤 Add user accounts and saved destinations.
- ❤️ Allow users to save favorite travel guides.
- 📱 Further optimize the interface for mobile devices.
- 🌐 Support additional languages and voice options.
- 📊 Add travel history and personalized recommendations.

---

## 🎓 Learning / Project Highlights

Building TravellingGuide provided practical experience in:

- 🎨 **Frontend Development** – Creating user interfaces using HTML, CSS, and JavaScript.
- ⚙️ **Backend Development** – Building REST API functionality using Python and Flask.
- 🔗 **API Integration** – Integrating external AI and text-to-speech APIs.
- 🤖 **AI Integration** – Using the Gemini API to generate travel-related content.
- 🔊 **Text-to-Speech Integration** – Using the Murf API for audio generation.
- 🔐 **Environment Variables** – Managing API credentials securely using `.env`.
- 🌐 **Frontend–Backend Communication** – Connecting a browser-based application with a Flask backend.
- 🐙 **Git & GitHub** – Managing source code and version history.
- ☁️ **Deployment** – Deploying the backend using Render and the frontend using Netlify.
- 🛠️ **Debugging & Problem Solving** – Identifying and resolving development and deployment issues.

---

## 👨‍💻 Author

### Manikanta Choppa

B.Tech Computer Science Engineering Student

🔗 **GitHub:** [github.com/manikanta33124](https://github.com/manikanta33124)

🔗 **Project Repository:** [TravellingGuide](https://github.com/manikanta33124/TravelGuide)

---

## 📄 License

This project is licensed under the **MIT License**.

