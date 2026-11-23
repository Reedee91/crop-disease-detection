 
# AI-Based Crop Disease Detection and Solution Recommendation System for Bangladeshi Farmers

An AI-powered web application designed to help Bangladeshi farmers detect crop diseases from leaf images and receive reliable disease information, treatment, and prevention guidance in Bangla and English.

<p align="center">
  <b>Project Team: CSE4104-7G-T02</b><br>
  Software Development III (CSE-4104) | Section: 7G<br>
  Northern University of Business and Technology Khulna
</p>

---

## 1. Project Overview

The **AI-Based Crop Disease Detection and Solution Recommendation System** is a web-based application that helps farmers identify crop diseases by uploading photographs of affected leaves.

The system uses a Convolutional Neural Network (CNN) with transfer learning to predict diseases of selected crops such as tomato, potato, and rice.

After prediction, the system displays the disease name and confidence score. If the prediction is sufficiently confident, the application retrieves verified treatment and prevention information from an agricultural knowledge base.

The guidance is available in both Bangla and English. If the prediction is uncertain, the system displays a warning and recommends consulting an agricultural expert.

**Main Concept:**

`Disease Detection → Explanation → Solution`

## 2. Project Objectives

- Detect selected crop diseases using AI and leaf images.
- Display disease predictions with confidence scores.
- Identify uncertain predictions and recommend expert consultation.
- Provide verified treatment and prevention guidance.
- Support both Bangla and English languages.
- Maintain users' disease detection history.
- Provide an administration dashboard for managing system information.

## 3. Proposed Features

### Farmer / Learner Features
- User registration and login.
- Upload crop leaf images.
- Image preview and validation.
- AI-based crop disease detection.
- Disease name and confidence score.
- Symptoms and possible causes.
- Treatment and management steps.
- Prevention measures.
- Bangla and English language support.
- View and manage detection history.
- Expert referral advice for uncertain results.

### Agricultural Expert Features
- View unverified knowledge-base entries.
- Review disease information and sources.
- Verify correct agricultural guidance.
- Return incorrect entries with review notes.

### Administrator Features
- Manage users and user status.
- Add and update crops.
- Add and update diseases.
- Manage treatment and prevention information.
- Manage agricultural knowledge sources.
- View detection statistics.
- Configure the AI confidence threshold.

## 4. Technology Stack

| Area | Technology |
|---|---|
| Frontend | React.js (Vite), JavaScript, HTML5, CSS3 |
| Backend | Django, Django REST Framework |
| Programming Language | Python, JavaScript |
| Database | PostgreSQL |
| AI Model | CNN / Transfer Learning |
| Model Options | MobileNetV2 / EfficientNet-Lite |
| Image Processing | OpenCV, Pillow |
| Model Deployment Format | ONNX / TensorFlow Lite |
| Optional AI Service | Google Gemini API |
| Dataset | PlantVillage, Public Rice Leaf Disease Dataset |
| Version Control | Git and GitHub |
| Frontend Deployment | Vercel |
| Backend Deployment | Render |

## 5. System Architecture

The system follows a client-server architecture.

- **Frontend:** React.js provides the user interface.
- **Backend:** Django and Django REST Framework handle authentication, image validation, disease detection, and business logic.
- **Database:** PostgreSQL stores users, crops, diseases, guidance, sources, detection history, and system settings.
- **AI Model:** A CNN-based model predicts crop diseases from processed leaf images.
- **Image Processing:** OpenCV and Pillow validate, resize, and normalize uploaded images.
- **Optional Gemini API:** Simplifies verified guidance into easy Bangla. It does not generate treatment recommendations.

### System Workflow

1. Farmer uploads a crop leaf image.
2. Backend validates the uploaded image.
3. OpenCV and Pillow check image quality and leaf suitability.
4. The image is resized and normalized.
5. The CNN model predicts the disease and confidence score.
6. Backend compares confidence with the configured threshold.
7. Verified guidance is retrieved from the PostgreSQL knowledge base when confidence is sufficient.
8. If confidence is low, the system shows an uncertainty warning and expert referral advice.
9. The detection result is saved in the user's history.

## 6. Database Design

The proposed database contains seven main tables:

| Table Name | Purpose |
|---|---|
| users | Stores user information, roles, and preferences |
| crops | Stores crop names in English and Bangla |
| diseases | Stores disease information and model class labels |
| disease_guidance | Stores symptoms, causes, treatment, and prevention |
| knowledge_sources | Stores agricultural information sources |
| detections | Stores prediction results and detection history |
| system_settings | Stores system configuration, including confidence threshold |

### Main Database Relationships

- One user can have many detection records.
- One crop can have many diseases.
- One disease can have multiple guidance entries.
- One disease can be predicted in many detection records.
- One knowledge source can support many guidance entries.
- One agricultural expert can verify many guidance entries.
- One administrator can update multiple system settings.

## 7. User Roles

The system has four main user roles:

1. **Guest:** Can register an account.
2. **Farmer / Learner:** Can upload images, detect diseases, view guidance, and manage detection history.
3. **Agricultural Expert:** Can review and verify agricultural knowledge-base entries.
4. **Administrator:** Can manage users, crops, diseases, guidance, sources, statistics, and system settings.

## 8. AI Integration

### Disease Detection Model

The system proposes using a CNN with transfer learning.

Possible models:
- MobileNetV2
- EfficientNet-Lite

The model receives a preprocessed leaf image and returns class probabilities. The backend selects the highest-probability class and displays its confidence score.

### Image Processing

OpenCV and Pillow are used for:
- Image format validation.
- Image quality checking.
- Leaf image checking.
- Resizing.
- Normalization.

### Confidence-Based Prediction

The system uses a configurable confidence threshold. The initial proposed default is approximately 75%.

- **Confident Prediction:** Retrieve verified disease guidance.
- **Uncertain Prediction:** Show a warning and recommend expert consultation.

The administrator can adjust the threshold based on validation results.

### Google Gemini API (Optional)

Gemini is used only to simplify already verified agricultural guidance into easy Bangla.

It must not independently generate treatment or pesticide recommendations.

If Gemini is unavailable, the system returns the original verified knowledge-base content.

## 9. Knowledge Base and Information Reliability

Treatment and prevention recommendations will be stored in a verified agricultural knowledge base.

Each guidance entry includes:
- Disease symptoms.
- Possible causes.
- Treatment and management steps.
- Prevention measures.
- Information source.
- Verification status.
- Expert review information.

Potential agricultural information sources include:

- Department of Agricultural Extension (DAE)
- Bangladesh Agricultural Research Institute (BARI)
- Bangladesh Rice Research Institute (BRRI)

Only expert-verified entries will be presented as verified guidance to farmers.

## 10. API Design

The backend will provide REST APIs using the base path:

`/api/v1`

Main API groups:

| API Group | Purpose |
|---|---|
| Authentication APIs | Registration, login, logout, token refresh |
| Profile APIs | View and update user profile |
| Detection APIs | Upload leaf image and predict disease |
| History APIs | View and delete detection history |
| Knowledge Base APIs | Retrieve crops, diseases, and guidance |
| Expert Review APIs | Verify or return knowledge-base entries |
| Administration APIs | Manage crops, diseases, users, sources, and settings |

Image uploads will use `multipart/form-data`. Other API requests and responses will generally use JSON.

Authentication will use JWT access tokens and role-based permissions.

## 11. AI Safety and Evaluation

The system will follow these safeguards:

- Display AI predictions with confidence scores and a disclaimer.
- Reject invalid or unsuitable images.
- Show uncertainty warnings for low-confidence predictions.
- Recommend agricultural expert consultation when necessary.
- Use verified agricultural information for treatment guidance.
- Keep Gemini API keys on the backend.
- Store the model version with each detection record.

### Model Evaluation

The proposed evaluation metrics are:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix

The target is at least **85% overall accuracy** on a held-out test set. This is a project target, not a claim of achieved performance.

Real field photographs will also be used for separate testing.

## 12. Project Scope

### Included in the First Version
- Web-based registration and login.
- Crop leaf image upload and validation.
- Selected tomato, potato, and rice disease detection.
- Confidence-aware prediction.
- Verified bilingual agricultural guidance.
- Expert review and referral.
- Detection history.
- Administrator dashboard.

### Outside the First Version
- Weather forecasting.
- Market price prediction.
- Crop profit prediction.
- Weather-based recommendations.
- Live expert chat.
- Online payments.
- Native mobile application.
- Pesticide and fertilizer sales or ordering.

## 13. Planned Repository Structure

```text
crop-disease-detection/
│
├── frontend/
│   └── React.js (Vite) application
│
├── backend/
│   ├── accounts/
│   ├── detections/
│   ├── knowledge/
│   ├── ai_services/
│   └── dashboard/
│
├── database/
│   ├── database schema
│   └── sample knowledge-base data
│
├── documentation/
│   ├── Proposal.pdf
│   ├── SRS.pdf
│   └── SystemDesign.pdf
│
├── diagrams/
│   ├── Architecture Diagram
│   ├── ER Diagram
│   ├── Use Case Diagram
│   └── Activity Diagrams
│
├── README.md
└── .gitignore
```

*Note: This is the planned project structure. Folders and files will be added as development progresses.*

## 14. Installation and Setup

The following setup steps are planned for the project.

### Prerequisites

- Python
- Node.js and npm
- PostgreSQL
- Git
- Visual Studio Code

### Clone the Repository

```bash
git clone https://github.com/Reedee91/crop-disease-detection.git
```

```bash
cd crop-disease-detection
```

### Frontend Setup

```bash
cd frontend
npm install
npm run dev
```

### Backend Setup

Open another terminal:

```bash
cd backend
```

Create a virtual environment:

```bash
python -m venv venv
```

Activate it on Windows:

```bash
venv\Scripts\activate
```

Install dependencies after the backend requirements file is created:

```bash
pip install -r requirements.txt
```

Run the Django development server:

```bash
python manage.py runserver
```

*Note: These commands are intended for the planned React and Django applications. They will work after the corresponding source files and configuration are added.*

## 15. Team Information

**Team Name:** CSE4104-7G-T02  
**Course:** Software Development III (CSE-4104)  
**Section:** 7G  
**Department:** Computer Science and Engineering  
**University:** Northern University of Business and Technology Khulna

| Student Name | Student ID | Responsibility | GitHub |
|---|---|---|---|
| Arnob Basak | 11230321491 | Team Leader & Team Coordination, System Analysis | [Basak725](https://github.com/Basak725) |
| Sheikh Mofazzal Hossain | 11230321472 | Frontend Development & User Interface | [SMHthree1](https://github.com/SMHthree1) |
| Subaita Kamal Reedee | 11230321291 | Backend Development & Database Management | [Reedee91](https://github.com/Reedee91) |
| Zareen Tasnim Mou | 11230321289 | AI/ML Model Development & Image Processing | [mou-1703](https://github.com/mou-1703) |

**Submitted To:**  
Md. Riaz Mahmud  
Assistant Professor, Department of CSE, NUBTK

## 16. Project Repository

GitHub Repository:

https://github.com/Reedee91/crop-disease-detection

## 17. References

1. Hughes, D. P., and Salathe, M. (2015). PlantVillage Dataset. https://arxiv.org/abs/1511.08060
2. Mohanty, S. P., Hughes, D. P., and Salathe, M. (2016). Using Deep Learning for Image-Based Plant Disease Detection. https://doi.org/10.3389/fpls.2016.01419
3. MobileNetV2. https://arxiv.org/abs/1801.04381
4. EfficientNet. https://arxiv.org/abs/1905.11946
5. Django Documentation. https://docs.djangoproject.com
6. Django REST Framework. https://www.django-rest-framework.org
7. PostgreSQL Documentation. https://www.postgresql.org/docs
8. OpenCV Documentation. https://docs.opencv.org
9. ONNX Runtime. https://onnxruntime.ai
10. Google Gemini API. https://ai.google.dev
11. React Documentation. https://react.dev
12. Vite Documentation. https://vite.dev
13. Department of Agricultural Extension (DAE). https://dae.gov.bd
14. Bangladesh Agricultural Research Institute (BARI). https://bari.gov.bd
15. Bangladesh Rice Research Institute (BRRI). https://brri.gov.bd

---

<p align="center">
  <b>AI-Based Crop Disease Detection and Solution Recommendation System</b><br>
  Developed by Team CSE4104-7G-T02
</p>
