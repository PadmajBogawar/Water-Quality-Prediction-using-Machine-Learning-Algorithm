# Water Quality Prediction and Monitoring using Machine Learning
Link : https://water-quality-frontend-seven.vercel.app/

A full-stack machine learning application for real-time water quality assessment and monitoring. This system predicts water potability and provides actionable recommendations based on WHO standards using ensemble ML models.

![Water Quality Dashboard](https://img.shields.io/badge/Status-Active-success)
![License](https://img.shields.io/badge/License-MIT-blue)
![Python](https://img.shields.io/badge/Python-3.8%2B-brightgreen)
![Next.js](https://img.shields.io/badge/Next.js-15.2.4-black)

## 📋 Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [System Architecture](#system-architecture)
- [Installation](#installation)
- [Usage](#usage)
- [Model Performance](#model-performance)
- [Screenshots](#screenshots)
- [Future Work](#future-work)
- [Contributing](#contributing)
- [License](#license)
- [Authors](#authors)

## 🌊 Overview

This project addresses the challenge of ensuring water safety through an automated, ML-driven solution that predicts water potability and detects quality fluctuations in real-time. The system analyzes critical water parameters such as pH, dissolved oxygen (DO), biological oxygen demand (BOD), conductivity, and nitrate levels to provide comprehensive water quality assessments.

**Key Highlights:**
- 87% prediction accuracy using LSTM-based models
- Real-time water quality monitoring
- WHO standard-based recommendations
- Interactive data visualization dashboard
- JWT-based secure authentication

## ✨ Features

### Core Functionality
- **Water Quality Prediction**: ML-powered potability assessment with 95% confidence
- **Real-Time Analysis**: Instant evaluation of water parameters against WHO standards
- **Actionable Recommendations**: Categorized immediate, short-term, and long-term actions
- **Trend Analysis**: 30-day historical data visualization for key parameters
- **PDF Report Generation**: Downloadable comprehensive water quality reports

### Technical Features
- **Ensemble ML Models**: Random Forest, XGBoost, Gradient Boosting
- **Data Preprocessing**: Cleaning, normalization, class balancing, feature engineering
- **Interactive Dashboard**: Real-time WQI, pH, temperature, and DO monitoring
- **Secure Authentication**: JWT tokens with bcrypt password hashing
- **Database Persistence**: PostgreSQL with SQLAlchemy ORM

## 🛠️ Tech Stack

### Frontend
- **Framework**: Next.js 15.2.4 with TypeScript
- **UI Components**: Radix UI, Tailwind CSS
- **Data Visualization**: Recharts, Plotly
- **Form Handling**: React Hook Form with Zod validation

### Backend
- **Framework**: FastAPI (Python)
- **ML Libraries**: TensorFlow, Keras, Scikit-learn, XGBoost
- **Database**: PostgreSQL with SQLAlchemy ORM
- **Authentication**: JWT, bcrypt

### Data Science
- **Models**: LSTM, Random Forest, XGBoost, Gradient Boosting
- **Techniques**: Class weighting, batch normalization, cross-validation
- **Visualization**: Matplotlib, Seaborn

## 🏗️ System Architecture

```
┌─────────────────┐         ┌──────────────────┐         ┌─────────────────┐
│   Frontend      │────────▶│   Backend API    │────────▶│   PostgreSQL    │
│   (Next.js)     │         │   (FastAPI)      │         │   Database      │
└─────────────────┘         └──────────────────┘         └─────────────────┘
                                     │
                                     ▼
                            ┌──────────────────┐
                            │   ML Models      │
                            │ - Random Forest  │
                            │ - XGBoost        │
                            │ - Gradient Boost │
                            └──────────────────┘
```

## 📦 Installation

### Prerequisites
- Python 3.8+
- Node.js 18+
- PostgreSQL 13+
- Git

### Backend Setup

```bash
# Clone the repository
git clone https://github.com/PadmajBogawar/water-quality-prediction.git
cd water-quality-prediction

# Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Set up database
createdb water_quality_db

# Configure environment variables
cp .env.example .env
# Edit .env with your database credentials

# Run database migrations
python init_db.py

# Start the backend server
uvicorn main:app --reload
```

### Frontend Setup

```bash
# Navigate to frontend directory
cd frontend

# Install dependencies
npm install

# Configure environment variables
cp .env.local.example .env.local
# Edit .env.local with your API endpoint

# Start the development server
npm run dev
```

The application will be available at:
- Frontend: `http://localhost:3000`
- Backend API: `http://localhost:8000`
- API Documentation: `http://localhost:8000/docs`

## 🚀 Usage

### 1. User Registration & Login
- Create an account or log in with existing credentials
- JWT tokens are used for secure session management

### 2. Submit Water Quality Measurements
Navigate to the "New Measurement" page and enter:
- Temperature (°C)
- pH level
- Dissolved Oxygen (mg/L)
- Conductivity (μS/cm)
- BOD (mg/L)
- Nitrate levels (mg/L)
- Coliform counts

### 3. View Analysis Results
- Water Quality Index (WQI) score
- Potability prediction with confidence level
- Parameter comparison with WHO standards
- Detailed recommendations

### 4. Monitor Trends
- View 30-day historical trends
- Analyze parameter fluctuations
- Export data for further analysis

### 5. Download Reports
Generate and download comprehensive PDF reports for record-keeping and compliance.

## 📊 Model Performance

### Feature Importance Ranking

| Feature | Importance Score |
|---------|-----------------|
| pH | 0.74 |
| Dissolved Oxygen | 0.07 |
| Conductivity | 0.04 |
| BOD | 0.02 |
| Nitrate | 0.02 |
| Temperature | 0.02 |

### Model Accuracy
- **LSTM Model**: 87% test accuracy
- **Random Forest**: 95% prediction confidence
- **Ensemble Models**: Improved reliability through class weighting and batch normalization

## 📸 Screenshots

### Dashboard Overview
![Dashboard](screenshots/dashboard.png)
*Real-time monitoring with WQI, pH, temperature, and DO levels*

### Analysis Results
![Analysis](screenshots/analysis.png)
*Comprehensive parameter analysis with ML predictions*

### Trend Visualization
![Trends](screenshots/trends.png)
*30-day historical data trends for key parameters*

## 🔮 Future Work

1. **IoT Integration**: Real-time data collection through IoT sensors
2. **Advanced ML Models**: Deep learning approaches for improved accuracy
3. **Geospatial Analysis**: GIS mapping for regional water quality visualization
4. **Mobile Application**: Native iOS and Android apps
5. **Predictive Forecasting**: Long-term water quality trend predictions
6. **Multi-language Support**: Internationalization for global deployment

## 👥 Author

**Padmaj Dilip Bogawar**
- [GitHub](https://github.com/PadmajBogawar)
- [LinkedIn](https://www.linkedin.com/in/padmajbogawar/)

**Institution:** Sinhgad College of Engineering, Pune
**Department:** Computer Engineering
**Academic Year:** 2024-2025

## 📞 Contact

For questions, suggestions, or collaborations:
- **Email**: pambogawar@gmail.com
- **LinkedIn**: [linkedin.com/in/padmajbogawar](https://www.linkedin.com/in/padmajbogawar/)
- **GitHub**: [github.com/PadmajBogawar](https://github.com/PadmajBogawar)


