# ☀️ UrjaGram - Solar Module & VET-OS Platform

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![React](https://img.shields.io/badge/Frontend-React%2019%20%2B%20Vite-61DAFB?logo=react)](https://react.dev/)
[![FastAPI](https://img.shields.io/badge/Backend-FastAPI-009688?logo=fastapi)](https://fastapi.tiangolo.com/)
[![TailwindCSS](https://img.shields.io/badge/Styling-TailwindCSS%203-38B2AC?logo=tailwind-css)](https://tailwindcss.com/)
[![PM Surya Ghar](https://img.shields.io/badge/Scheme-PM%20Surya%20Ghar-orange)](https://pmsuryaghar.gov.in)

> **UrjaGram** is a unified Digital Aggregator & Virtual Energy Transition Operating System (VET-OS) accelerating rooftop solar deployment under India's **PM Surya Ghar: Muft Bijli Yojana** (1 Crore Homes initiative). 
> It shortens the solar installation-to-subsidy lifecycle from **60+ days to under 15 days** using automated financing, AI rooftop & demand assessment, RPA integration, and strict Domestic Content Requirement (DCR) compliance.

---

## 🌟 Key Features & Capabilities

- **🔍 AI-Powered Solar & Rooftop Assessment**:
  - Instant rooftop sizing, shading estimation, and solar generation capacity computation.
  - Live Peak Sun Hours integration via Google Earth Engine (GEE).
  - Monthly electricity consumption prediction based on household appliance load profiles.
- **⚡ Zero-Defect KYC & Document Validation**:
  - Automated pre-check for Aadhaar, electricity bills, and bank accounts to eliminate name/IFSC mismatches before submission.
- **🤖 GOI Portal Sync (RPA Automation)**:
  - Automated pre-submission pipeline syncing validated application packages directly with `pmsuryaghar.gov.in`.
- **🤝 Smart Empanelled Vendor Matchmaking**:
  - Match consumers with verified DISCOM & MNRE empanelled vendors with guaranteed DCR-certified inventory.
- **💳 Instant Digital Lending (LaaS - Lending-as-a-Service)**:
  - Parallel financing workflows with Green NBFCs to secure 1-click loan approvals while DISCOM feasibility is underway.
- **📊 Village & MRV Dashboard**:
  - Comprehensive rural energy transition planning, carbon offset tracking, and clean energy analytics.

---

## 🏗️ Architecture & Tech Stack

### Frontend
- **Framework**: [React 19](https://react.dev/) with [Vite](https://vitejs.dev/)
- **UI & Animations**: Tailwind CSS, Lucide Icons, Framer Motion
- **3D & Visualizations**: Three.js, React Three Fiber, Recharts, Leaflet
- **Database / Backend-as-a-Service**: Supabase

### Backend
- **Framework**: Python [FastAPI](https://fastapi.tiangolo.com/) & Uvicorn
- **AI & Analytics**: Scikit-Learn, Pandas, Joblib (Electricity Demand Forecasting Model)
- **Geospatial Analysis**: Google Earth Engine API (`earthengine-api`)

---

## 📂 Project Structure

```text
UrjaGram/
├── src/                          # React Frontend Application
│   ├── components/               # Core feature modules (SolarAssessment, GoiRpaSync, VillageMap, etc.)
│   ├── contexts/                 # App context providers (Language, Auth, etc.)
│   ├── data/                     # Solar LUT, state benchmarks, and tariff engines
│   └── utils/                    # Calculations, AI vision, and Supabase integration
├── backend/                      # FastAPI Python Service
│   ├── main.py                   # API routes and server entry point
│   ├── schemas.py                # Pydantic request/response models
│   ├── predictor.py              # ML demand forecasting model loader
│   ├── electricity_model.pkl     # Pre-trained ML model
│   └── requirements.txt          # Python dependencies
├── gee_solar_analysis.ipynb      # Google Earth Engine solar irradiance notebook
├── supabase_migration.sql        # Database schema and table definitions
├── package.json                  # Frontend dependencies and scripts
└── UrjaGram_MNRE_Pitch.md        # Ministry of New & Renewable Energy presentation doc
```

---

## 🚀 Quick Start Guide

### 1. Prerequisites
- **Node.js**: v18+ installed
- **Python**: v3.10+ installed
- **Git**

### 2. Frontend Setup
```bash
# Clone the repository
git clone https://github.com/UrjaGram/Solar-Module.git
cd Solar-Module

# Install frontend dependencies
npm install

# Start development server
npm run dev
```

### 3. Backend Setup
```bash
# Navigate to backend directory
cd backend

# Create virtual environment
python -m venv venv
# On Windows:
venv\Scripts\activate
# On Linux/macOS:
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Start FastAPI server
uvicorn main:app --reload --port 8000
```

---

## ⚙️ Environment Variables

Create a `.env` file in the root directory for frontend configurations:
```env
VITE_SUPABASE_URL=your_supabase_url
VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
VITE_OPENAI_API_KEY=your_optional_openai_key
```

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the issues page or submit a pull request.

---

## 📄 License

This project is licensed under the MIT License.
