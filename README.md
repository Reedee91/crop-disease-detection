
# 🌱 AI-Based Crop Disease Detection and Recommendation System

## 📌 Project Description

The AI-Based Crop Disease Detection and Recommendation System is a web-based application that uses Artificial Intelligence to identify possible crop diseases from leaf images.

Users can upload images of crop leaves, and the AI model will analyze the images to predict possible diseases. The system will also provide disease information, symptoms, and basic treatment recommendations.

This project aims to help farmers and other users identify crop diseases more easily and support early disease detection.

## 🎯 Project Objectives

- Develop an AI-based crop disease detection system.
- Identify diseases from crop leaf images.
- Apply image processing using OpenCV and Pillow.
- Predict disease names with confidence scores.
- Provide basic treatment and prevention suggestions.
- Maintain previous disease detection records.

## ✨ Proposed Features

1. User Registration and Login
2. User Dashboard
3. Crop Leaf Image Upload
4. AI-Based Disease Prediction
5. Disease Name and Confidence Score
6. Disease Symptoms and Treatment Suggestions
7. Disease Detection History
8. Basic Admin Dashboard

## 🛠️ Technology Stack

| Component | Technology |
|---|---|
| Frontend | React.js |
| Backend | Python, Django |
| API | Django REST Framework |
| Database | PostgreSQL |
| AI Model | Convolutional Neural Network (CNN) |
| Image Processing | OpenCV, Pillow |
| Dataset | PlantVillage |
| Version Control | Git, GitHub |
| Code Editor | Visual Studio Code |

## 🤖 AI Integration

The system will use a CNN-based image classification model to identify possible crop diseases.

OpenCV and Pillow will be used to preprocess uploaded leaf images before sending them to the AI model.

The model will analyze the images and predict the possible disease along with a confidence score.

## 🔄 Proposed Workflow

1. User uploads a crop leaf image.
2. The image is processed using OpenCV and Pillow.
3. The CNN model analyzes the image.
4. The system predicts the possible crop disease.
5. Django REST API sends the prediction result.
6. React.js displays the result to the user.
7. Detection history is stored in PostgreSQL.

## 🌾 Initial Project Scope

The initial version will focus on selected diseases of:

- Tomato
- Potato
- Rice

The system will also include healthy leaf categories where suitable datasets are available.

## 👥 Team Information

**Team Name:** CSE4104-[Section]-T[TeamNumber]

**Course Code:** CSE4104

**Department:** Computer Science and Engineering

**Institution:** [University Name]

### Team Members

| No. | Name | Responsibility |
|---|---|---|
| 1 | Subaita Kamal Reedee | Team Leader & Frontend |
| 2 | [Member 2 Name] | Backend Development |
| 3 | [Member 3 Name] | AI Model Development |
| 4 | [Member 4 Name] | Database, Testing & Documentation |

## 📂 Project Structure

```text
crop-disease-detection/
│
├── frontend/
│
├── backend/
│
├── ai_model/
│
├── documentation/
│
└── README.md
```

## 🚀 Expected Outcome

A functional web application that can analyze selected crop leaf images, predict possible diseases, display confidence scores, and provide basic disease information and recommendations.

## ⚠️ Disclaimer

This project is developed for educational and preliminary crop disease identification purposes. Its predictions should not replace professional agricultural advice.

## 📌 Project Status

Currently in the initial planning and development stage.
