 
# AI-Based Crop Disease Detection and Solution Recommendation System for Bangladeshi Farmers

An AI-powered web application designed to help Bangladeshi farmers identify crop diseases from leaf images and receive verified treatment and prevention guidance.

## 🔗 GitHub Repository

https://github.com/Reedee91/crop-disease-detection

---

## 📌 Project Information

| Field | Details |
|---|---|
| Project Title | AI-Based Crop Disease Detection and Solution Recommendation System for Bangladeshi Farmers |
| Course Code | CSE 4104 |
| Course Title | Software Development III |
| Team Name | CSE4104-7G-T02 |
| Section | 7G |
| Department | Computer Science and Engineering |
| University | Northern University of Business and Technology Khulna |

---

## 👥 Team Members

| Name | Student ID | Responsibility |
|---|---|---|
| Arnob Basak (Team Leader) | 11230321491 | Team Coordination and System Analysis |
| Sheikh Mofazzal Hossain | 11230321472 | Frontend Development and UI Design |
| Subaita Kamal Reedee | 11230321291 | Backend Development and Database |
| Zareen Tasnim Mou | 11230321289 | AI/ML Model and Image Processing |

---

## 📖 Project Description

Crop diseases are one of the major challenges faced by farmers in Bangladesh. Many farmers struggle to identify diseases at an early stage and often do not know the correct treatment and prevention methods.

Our project aims to develop an AI-based web application that helps farmers identify crop diseases using photographs of affected plant leaves.

Users can upload leaf images to the system. The system validates and preprocesses the images before using a CNN or transfer-learning model to predict the most likely disease and display a confidence score.

After prediction, the system retrieves relevant information from a verified agricultural knowledge base. It provides disease symptoms, causes, treatment steps, and prevention measures in simple Bangla and English.

If the prediction confidence is low, the system displays an uncertainty warning and recommends consulting an agricultural expert.

**Main Concept: Disease Detection → Explanation → Solution Recommendation**

---

## 🎯 Project Objectives

- Detect selected crop diseases using AI.
- Display prediction results with confidence scores.
- Provide verified treatment and prevention guidance.
- Support both Bangla and English languages.
- Recommend agricultural expert consultation when necessary.
- Maintain users' previous detection records.
- Provide an admin dashboard for system management.

---

## 🚀 Proposed Features

### 1. User Management
- User registration and login.
- User profile management.
- Password change and logout.
- Role-based access control.

### 2. Leaf Image Upload and Validation
- Upload leaf images from a device gallery or camera.
- Preview selected images before submission.
- Support JPG, JPEG, and PNG formats.
- Maximum image size: 5 MB.
- Check image quality, blur, and resolution.
- Reject unrelated images that are not plant leaves.

### 3. AI-Based Disease Detection
- Analyze uploaded leaf images.
- Use CNN or transfer-learning models.
- Detect selected diseases of tomato, potato, and rice.
- Identify healthy leaf classes where datasets are available.
- Display predicted disease names and confidence scores.
- Show uncertainty warnings for low-confidence predictions.

### 4. Disease Information and Solution
- Display disease symptoms and causes.
- Provide treatment and management steps.
- Show prevention measures.
- Retrieve guidance from a verified agricultural knowledge base.
- Record the sources of agricultural information.

### 5. Bangla and English Support
- Display disease information in Bangla and English.
- Provide a language selection option.
- Use simple and understandable language.

### 6. Expert Referral
- Recommend agricultural expert consultation for uncertain predictions.
- Suggest expert consultation for severe infections.
- Allow experts to review and verify knowledge-base entries.

### 7. Detection History
- Save previous disease detection results.
- View previous detection records.
- Display the newest records first.
- Allow users to filter and delete their own records.

### 8. Admin Dashboard
- Manage crop and disease information.
- Add and update treatment and prevention guidance.
- Manage registered users.
- View basic system statistics.
- Configure the confidence threshold.
- Record knowledge-base information sources.

---

## 🛠️ Proposed Technology Stack

| Category | Technology |
|---|---|
| Frontend | React.js (Vite) |
| Backend | Python, Django |
| API | Django REST Framework |
| Database | PostgreSQL |
| AI/ML Model | CNN / Transfer Learning |
| Image Processing | OpenCV, Pillow |
| Dataset | PlantVillage and other suitable public datasets |
| Optional AI Service | Google Gemini API |
| Version Control | Git and GitHub |
| Code Editor | Visual Studio Code |

*Note: These are the proposed technologies for the project.*

---

## 🤖 AI Integration

The system will use a CNN or transfer-learning model to identify crop diseases from uploaded leaf images.

### AI Detection Process

1. Receive the uploaded leaf image.
2. Validate image format, size, and quality.
3. Preprocess the image using OpenCV or Pillow.
4. Send the processed image to the trained AI model.
5. Predict the most likely disease.
6. Calculate and display the confidence score.

### Confidence Threshold

The default confidence threshold will be approximately 75%. The administrator can configure this threshold.

### Google Gemini API (Optional)

The Gemini API may be used only to simplify or translate verified knowledge-base information.

It will not independently generate treatment or prevention advice. If Gemini is unavailable, the system will display the stored knowledge-base information.

---

## 🔄 Proposed System Workflow

1. User registers or logs into the system.
2. User uploads a crop leaf image.
3. The system validates the image.
4. The image is preprocessed.
5. The AI model predicts the disease.
6. The system displays the disease name and confidence score.
7. Related information is retrieved from the verified knowledge base.
8. Symptoms, causes, treatment, and prevention guidance are displayed.
9. If confidence is low, an expert consultation warning is shown.
10. The detection result is saved in the user's history.

---

## 🌱 Initial Project Scope

The first version will focus on selected diseases of:

- Tomato
- Potato
- Rice

Healthy leaf classes will also be included where suitable datasets are available.

### Out of Scope for the First Version

- Weather forecasting.
- Market-price prediction.
- Crop-profit prediction.
- Weather-based recommendations.
- Other crops beyond the selected classes.
- Live chat with agricultural experts.
- Online payments.
- Native mobile applications.
- Pesticide or fertilizer sales and automatic ordering.

---

## 📚 Agricultural Knowledge Base

The system will maintain a verified agricultural knowledge base containing:

- Crop information.
- Disease names.
- Disease symptoms.
- Disease causes.
- Treatment and management steps.
- Prevention measures.
- Information sources.

Potential information sources include:

- Department of Agricultural Extension (DAE).
- Bangladesh Agricultural Research Institute (BARI).
- Bangladesh Rice Research Institute (BRRI).

Knowledge-base entries will be reviewed by agricultural experts before being marked as verified.

---

## 📁 Proposed Project Structure

```text
crop-disease-detection/
│
├── frontend/
│   ├── public/
│   └── src/
│
├── backend/
│   ├── manage.py
│   └── requirements.txt
│
├── ai_model/
│   ├── dataset/
│   ├── training/
│   └── models/
│
├── documentation/
│   ├── SRS.pdf
│   └── diagrams/
│
├── README.md
└── .gitignore
```

*The project structure may change during development.*

---

## 🔐 Security and Reliability

- Passwords will be stored using secure password hashing.
- Protected pages and APIs will require authentication.
- Role-based access control will be implemented.
- Uploaded images will be validated.
- API keys and database credentials will be stored in environment variables.
- Users will only access their own detection history.
- The system will handle errors if the model, database, or optional Gemini API is unavailable.

---

## 📅 Development Plan

| Phase | Activities |
|---|---|
| Phase 1 | Requirement Analysis and SRS Documentation |
| Phase 2 | System Design and Database Design |
| Phase 3 | Frontend Development |
| Phase 4 | Backend and API Development |
| Phase 5 | Dataset Preparation and AI Model Training |
| Phase 6 | AI Model and Backend Integration |
| Phase 7 | Testing and Evaluation |
| Phase 8 | Final Deployment and Documentation |

---

## 📊 Expected Outcome

The expected outcome is a user-friendly web application that helps Bangladeshi farmers identify selected crop diseases through leaf images and understand possible solutions using verified agricultural information.

The system aims to support early disease identification, provide accessible agricultural guidance, and encourage consultation with agricultural experts when necessary.

---

## ⚠️ Disclaimer

The system provides preliminary crop disease identification only. AI predictions may not always be accurate, particularly for real-world field images. It does not replace professional agricultural advice. Farmers should consult an agricultural expert before making important treatment decisions.

---

## 📌 Project Status

**Status:** Planning and Development

This project is being developed as part of the Software Development III (CSE 4104) course.

---

## 👨‍💻 Developed By

**Team CSE4104-7G-T02**

Department of Computer Science and Engineering  
Northern University of Business and Technology Khulna
