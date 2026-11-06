 
# 🌱 AI-Based Crop Disease Detection and Solution Recommendation System for Bangladeshi Farmers

**Course:** CSE4104  
**Team:** CSE4104-7G-T02  
**Section:** 7G  
**Department:** Computer Science and Engineering  
**Institution:** Northern University of Business and Technology Khulna

---

## 📌 Project Description

The AI-Based Crop Disease Detection and Solution Recommendation System is an AI-powered web application designed to help farmers in Bangladesh identify crop diseases from leaf images and receive practical guidance on how to manage them.

Users can upload an image of an affected crop leaf. The AI model analyzes the image and predicts the most likely disease along with a confidence score.

The system then provides disease information, symptoms, possible causes, recommended management steps, and preventive measures using a verified agricultural knowledge base.

The main focus of this project is:

**Disease → Explanation → Solution**

This project aims to support early crop disease identification and help farmers make more informed agricultural decisions.

## ❗ Real-World Problem

Small and medium-scale farmers in Bangladesh often face several challenges:

- Difficulty identifying crop diseases from visual symptoms.
- Lack of knowledge about appropriate disease management.
- Limited quick access to agricultural experts.
- Uncertainty about preventive agricultural practices.
- Difficulty finding reliable and understandable disease information.

Many existing solutions focus mainly on disease identification without providing a simple and practical path from diagnosis to solution.

Artificial Intelligence can help address this problem by analyzing crop leaf images and providing preliminary disease predictions.

## 🎯 Project Objectives

- Develop an AI-based crop disease detection system.
- Identify selected crop diseases from leaf images.
- Display disease predictions with confidence scores.
- Apply image preprocessing using OpenCV and Pillow.
- Provide verified treatment and prevention guidance.
- Refer uncertain cases to agricultural experts.
- Maintain previous disease detection records.
- Develop a simple and user-friendly web application.

## ✨ Core Features

### A. Farmer Account Management

- Farmer registration and secure login.
- Basic user profile management.

### B. Crop Image Upload and AI Disease Detection

- Upload images of affected crop leaves.
- CNN-based disease prediction.
- Display predicted disease names and confidence scores.

### C. Disease Information and Solution Recommendation

- Disease names and affected crop information.
- Symptoms and possible causes.
- Practical disease management steps.
- Preventive agricultural practices.

### D. Expert Referral

- Identify low-confidence predictions.
- Recommend consulting an agricultural expert when the result is uncertain.

### E. Detection History

- Save previous disease detection results.
- Allow users to review their detection history.

### F. Admin Dashboard

- Manage crop information.
- Manage disease information and symptoms.
- Manage treatment and prevention recommendations.
- Manage registered users.

## 🤖 AI Integration

The system will use a Convolutional Neural Network (CNN) or a transfer-learning model to classify crop leaf images.

OpenCV and Pillow will be used to preprocess uploaded images before prediction.

The AI model will predict the most likely disease and provide a confidence score.

Treatment and prevention recommendations will be retrieved from a verified agricultural knowledge base instead of relying on freely generated AI responses.

If the model produces a low-confidence prediction, the system will display an uncertainty warning and recommend consulting an agricultural expert.

**Optional AI Integration:** Google Gemini API may be used in a future version to explain disease information in simple Bangla.

## 🔄 Proposed Workflow

1. The user uploads a crop leaf image.
2. OpenCV and Pillow preprocess the uploaded image.
3. The CNN model analyzes the processed image.
4. The model predicts the most likely disease and confidence score.
5. The predicted disease is matched with the agricultural knowledge base.
6. Django REST API sends the result to the frontend.
7. React.js displays the disease explanation, management steps, and prevention guidance.
8. Low-confidence results are flagged for expert consultation.
9. Detection information is stored in PostgreSQL.

## 🛠️ Technology Stack

| Component | Technology |
|---|---|
| Frontend | React.js (Vite) |
| Backend | Python, Django |
| API | Django REST Framework |
| Database | PostgreSQL |
| AI Model | CNN / Transfer Learning |
| Image Processing | OpenCV, Pillow |
| Dataset | PlantVillage and other suitable public datasets |
| AI Assistant (Optional) | Google Gemini API |
| Version Control | Git, GitHub |
| Code Editor | Visual Studio Code |

### Supporting Languages

- Python
- JavaScript
- HTML
- CSS
- SQL

## 🌾 Initial Project Scope

The initial version will focus on selected diseases of:

- Tomato
- Potato
- Rice

Healthy leaf categories will also be included where suitable datasets are available.

The project will initially focus on image-based disease identification and basic disease management recommendations.

### Features Outside the Initial Scope

- Weather forecasting.
- Market-price prediction.
- Crop-profit prediction.
- General weather-based recommendations.

These features may be considered for future development if time permits.

## 📂 Project Structure

```text
crop-disease-detection/
│
├── frontend/                 # React.js application
│
├── backend/                  # Django backend and REST API
│
├── ai_model/                 # CNN training and prediction
│
├── documentation/            # Proposal, reports and diagrams
│
└── README.md                 # Project documentation
```

## 🚀 Getting Started

### Prerequisites

Make sure the following software is installed:

- Python 3.x
- pip
- Node.js (LTS version)
- npm
- PostgreSQL
- Git
- Visual Studio Code

### 1. Clone the Repository

```bash
git clone https://github.com/Reedee91/crop-disease-detection.git

cd crop-disease-detection
```

### 2. Backend Setup (Django)

Open a terminal in the project root directory.

```bash
cd backend
```

Create a Python virtual environment:

```bash
python -m venv venv
```

Activate the virtual environment on Windows:

```bash
venv\Scripts\activate
```

Install the required Python packages:

```bash
pip install -r requirements.txt
```

Run database migrations:

```bash
python manage.py migrate
```

Start the Django development server:

```bash
python manage.py runserver
```

Backend server:

http://127.0.0.1:8000/

### 3. Frontend Setup (React.js with Vite)

Open a new terminal in the project root directory.

```bash
cd frontend
```

Install frontend dependencies:

```bash
npm install
```

Start the React development server:

```bash
npm run dev
```

Frontend development server:

http://localhost:5173/

### 4. Database Configuration

PostgreSQL must be installed and configured before running database migrations.

Create a PostgreSQL database and configure the following settings in Django:

- Database Name
- Database User
- Database Password
- Database Host
- Database Port

Database credentials should be stored securely using environment variables rather than committed to GitHub.

**Note:** The Django project, `requirements.txt`, and Vite React application must be created before running their respective installation commands.

## 🗓️ Development Plan

| Phase | Planned Activities |
|---|---|
| Phase 1 | Project setup, requirement analysis and system design |
| Phase 2 | Crop and disease selection, dataset collection and preparation |
| Phase 3 | Image preprocessing and CNN model development |
| Phase 4 | Model evaluation and backend API development |
| Phase 5 | Frontend development and database integration |
| Phase 6 | Knowledge base, detection history and expert referral |
| Phase 7 | System integration, testing and deployment |

## 👥 Team Information

**Team Name:** CSE4104-7G-T02

**Course Code:** CSE4104

**Section:** 7G

**Department:** Computer Science and Engineering

**Institution:** Northern University of Business and Technology Khulna

### Team Members

| No. | Name | Student ID | Responsibility |
|---|---|---|---|
| 1 | Arnob Basak (Team Leader) | 11230321491 | Team Coordination and System Analysis |
| 2 | Sheikh Mofazzal Hossain | 11230321472 | Frontend and User Interface |
| 3 | Subaita Kamal Reedee | 11230321291 | Backend and Database |
| 4 | Zareen Tasnim Mou | 11230321289 | AI/ML Model and Image Processing |

## 🚀 Expected Outcome

The expected outcome is a user-friendly web application that allows farmers to:

- Upload crop leaf images.
- Identify possible crop diseases using AI.
- View disease predictions and confidence scores.
- Understand disease symptoms and possible causes.
- Receive basic treatment and prevention recommendations.
- Get an expert referral suggestion when predictions are uncertain.
- Review previous disease detection records.

Administrators will be able to manage crop, disease, symptom, and solution information.

The project aims to make preliminary crop disease identification more accessible and useful for Bangladeshi farmers.

## ⚠️ Disclaimer

This project is developed for educational and preliminary crop disease identification purposes.

AI predictions may not always be accurate. Recommendations should be treated as general guidance and verified with qualified agricultural experts before taking important treatment decisions.

## 📌 Project Status

Currently in the initial planning and development stage.

---

**Developed by:** CSE4104-7G-T02  
**Department of Computer Science and Engineering**  
**Northern University of Business and Technology Khulna**