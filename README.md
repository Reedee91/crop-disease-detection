 
# 🌱 AI-Based Crop Disease Detection and Solution Recommendation System for Bangladeshi Farmers

**Team Name:** CSE4104-7G-T02  
**Course Code:** CSE4104  
**Section:** 7G  
**Department:** Computer Science and Engineering  
**Institution:** Northern University of Business and Technology Khulna

---

## 1. Project Title

**AI-Based Crop Disease Detection and Solution Recommendation System for Bangladeshi Farmers**

**Project Focus:** Disease → Explanation → Solution

## 2. Project Description

The AI-Based Crop Disease Detection and Solution Recommendation System is an AI-powered web application designed to help farmers in Bangladesh identify crop diseases from leaf images and receive practical management recommendations.

Farmers can upload an image of an affected crop leaf. The AI model analyzes the image and predicts the possible disease with a confidence score.

Based on the prediction, the system provides disease information, symptoms, possible causes, treatment guidance, and preventive measures using a verified agricultural knowledge base.

The main goal of this project is to make preliminary crop disease identification easier and more accessible for Bangladeshi farmers.

## 3. Problem Statement

Agriculture is an important part of Bangladesh's economy, and crop diseases can cause significant losses for farmers.

Small and medium-scale farmers often face difficulties identifying crop diseases from visual symptoms. They may also lack access to reliable disease information, appropriate management guidance, and agricultural experts.

Some existing disease detection solutions focus mainly on identifying diseases but do not provide sufficient practical guidance about what farmers should do next.

Artificial Intelligence can help address these challenges by analyzing crop leaf images and providing preliminary disease predictions.

Therefore, we propose an AI-based system that combines crop disease detection with understandable disease information, management recommendations, and preventive guidance.

## 4. Project Objectives

- Develop an AI-based crop disease detection system.
- Identify selected crop diseases from leaf images.
- Display predicted disease names with confidence scores.
- Apply image preprocessing techniques.
- Provide disease information, symptoms, and possible causes.
- Recommend practical disease management and prevention steps.
- Identify uncertain predictions and suggest expert consultation.
- Develop a simple and user-friendly web application.
- Maintain previous disease detection records.

## 5. Proposed Features

### A. Farmer Account Management
- Farmer registration and secure login.
- Basic user profile management.

### B. Crop Image Upload
- Upload images of affected crop leaves.
- Support image-based disease analysis.

### C. AI-Based Disease Detection
- CNN-based crop disease prediction.
- Display predicted disease names.
- Show prediction confidence scores.

### D. Disease Information
- Disease names and affected crop information.
- Symptoms and possible causes.
- Basic disease explanations.

### E. Solution Recommendation
- Practical disease management guidance.
- Treatment recommendations from a verified agricultural knowledge base.
- Preventive measures to reduce future disease risks.

### F. Expert Referral
- Identify low-confidence predictions.
- Recommend consultation with agricultural experts when results are uncertain.

### G. Detection History
- Save previous detection results.
- Allow users to review their detection history.

### H. Admin Dashboard
- Manage crop information.
- Manage disease information and symptoms.
- Manage treatment and prevention recommendations.
- Manage registered users.

## 6. Technology Stack

| Component | Technology |
|---|---|
| Frontend | React.js (Vite) |
| Backend | Python, Django |
| API | Django REST Framework |
| Database | PostgreSQL |
| AI Model | CNN / Transfer Learning |
| Image Processing | OpenCV, Pillow |
| Dataset | PlantVillage and other suitable public datasets |
| Optional AI Assistant | Google Gemini API |
| Version Control | Git and GitHub |
| Code Editor | Visual Studio Code |

### Programming Languages
- Python
- JavaScript
- HTML
- CSS
- SQL

## 7. AI Integration

The system will use a Convolutional Neural Network (CNN) or a transfer-learning model to classify crop leaf images.

OpenCV and Pillow will be used to preprocess uploaded images before sending them to the AI model.

The model will predict the most likely disease and provide a confidence score.

Disease information, symptoms, treatment guidance, and preventive measures will be retrieved from a verified agricultural knowledge base.

If the model produces a low-confidence prediction, the system will display an uncertainty warning and recommend consulting an agricultural expert.

**Optional AI Integration:** Google Gemini API may be used to explain disease information in simple Bangla.

## 8. Proposed System Workflow

1. The farmer uploads a crop leaf image.
2. OpenCV and Pillow preprocess the image.
3. The CNN model analyzes the processed image.
4. The model predicts the possible disease and confidence score.
5. The predicted disease is matched with the agricultural knowledge base.
6. Django REST API sends the result to the frontend.
7. React.js displays disease information, management guidance, and prevention steps.
8. Low-confidence predictions are flagged for expert consultation.
9. Detection results are stored in the PostgreSQL database.

## 9. Initial Project Scope

The initial version of the project will focus on selected diseases of:

- Tomato
- Potato
- Rice

Healthy leaf categories will also be included where suitable datasets are available.

The first version will focus on image-based disease identification and basic disease management recommendations.

### Features Outside the Initial Scope

- Weather forecasting.
- Market-price prediction.
- Crop-profit prediction.
- Weather-based agricultural recommendations.

These features may be considered for future development if time permits.

## 10. Project Structure

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

## 11. Development Plan

| Phase | Planned Activities |
|---|---|
| Phase 1 | Project setup, requirement analysis and system design |
| Phase 2 | Crop and disease selection, dataset collection and preparation |
| Phase 3 | Image preprocessing and CNN model development |
| Phase 4 | Model training, evaluation and backend API development |
| Phase 5 | Frontend development and database integration |
| Phase 6 | Knowledge base, detection history and expert referral |
| Phase 7 | System integration, testing and deployment |

## 12. Expected Outcome

The expected outcome is a user-friendly web application that allows farmers to:

- Upload crop leaf images.
- Identify possible crop diseases using AI.
- View disease predictions and confidence scores.
- Understand disease symptoms and possible causes.
- Receive practical disease management recommendations.
- Learn preventive agricultural practices.
- Get an expert referral suggestion when predictions are uncertain.
- Review previous disease detection records.

The project aims to make preliminary crop disease identification more accessible and useful for Bangladeshi farmers.

## 13. Team Information

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

## 14. Getting Started

### Prerequisites

Make sure the following software is installed:

- Python 3.x
- pip
- Node.js (LTS version)
- npm
- PostgreSQL
- Git
- Visual Studio Code

### Clone the Repository

```bash
git clone https://github.com/Reedee91/crop-disease-detection.git

cd crop-disease-detection
```

### Backend Setup (Django)

```bash
cd backend

python -m venv venv

venv\Scripts\activate

pip install -r requirements.txt
```

After configuring the PostgreSQL database and creating the Django project:

```bash
python manage.py migrate

python manage.py runserver
```

Backend server:

http://127.0.0.1:8000/

### Frontend Setup (React.js with Vite)

Open another terminal:

```bash
cd frontend

npm install

npm run dev
```

Frontend development server:

http://localhost:5173/

**Note:** These setup commands will work after the Django backend, `requirements.txt`, and React Vite application have been created. PostgreSQL must also be configured before running migrations.

## 15. Future Improvements

- Support for additional crops and diseases.
- Improved AI model accuracy with more diverse datasets.
- Bangla language support for farmers.
- Agricultural expert consultation features.
- More detailed disease management information.

## 16. Disclaimer

This project is developed for educational and preliminary crop disease identification purposes.

AI predictions may not always be accurate. Recommendations should be treated as general guidance and verified with qualified agricultural experts before taking important treatment decisions.

---

**Developed by:** CSE4104-7G-T02  
**Department of Computer Science and Engineering**  
**Northern University of Business and Technology Khulna**
