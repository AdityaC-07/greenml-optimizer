# 🌱 GreenML Optimizer

<div align="center">

![GreenML Optimizer](https://img.shields.io/badge/AI-Powered-green?style=for-the-badge)
![React](https://img.shields.io/badge/React-18.0+-blue?style=for-the-badge&logo=react)
![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)

**AI-powered carbon calculator for machine learning workloads**

Predict, analyze, and reduce carbon emissions from your ML training jobs.

[Live Demo](https://greenml-optimizer-jhn6-oczxf4nzw-aditya-choudhuris-projects.vercel.app/) 
</div>

---

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [API Documentation](#api-documentation)
- [Deployment](#deployment)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

---

## 🌍 Overview

GreenML Optimizer is an innovative solution designed to help data scientists and ML engineers understand and reduce the carbon footprint of their machine learning workloads. By leveraging advanced prediction models, it forecasts carbon emissions before job execution, enabling smarter, more sustainable AI development.

### Why GreenML Optimizer?

- 🌱 **Environmental Impact**: Training large ML models can emit as much CO2 as 5 cars in their lifetime
- 💰 **Cost Savings**: Optimized workloads = reduced cloud computing costs
- 📊 **Data-Driven**: Make informed decisions based on real carbon emission predictions
- 🎯 **Easy Integration**: Simple API and intuitive dashboard

---

## 🚀 Features

### Core Capabilities

- **🤖 AI Workload Optimization**
  - Smart resource allocation for ML workloads
  - GPU/CPU utilization recommendations
  - Batch size and training configuration suggestions

- **📈 Carbon Emission Prediction**
  - Forecast environmental impact before job execution
  - Region-based carbon intensity analysis
  - Model architecture impact assessment

- **📊 Real-time Dashboard**
  - Interactive carbon footprint visualizations
  - Historical tracking and trends
  - Comparative analysis across workloads

- **💚 Carbon & Cost Savings**
  - Track reduction in CO2 emissions
  - Monitor cloud cost savings
  - Generate sustainability reports

### Additional Features

- 🔄 Job history tracking
- 🌐 Multi-region support
- 📱 Responsive design
- 🎨 Clean, modern UI
- 📥 Export reports (CSV/PDF)

---

## 🛠️ Tech Stack

### Frontend
- **React 18+** - UI framework
- **Bootstrap 5** - Responsive design
- **Recharts** - Data visualization
- **Lucide React** - Modern icons
- **Axios** - HTTP client

### Backend (API Server)
- **Flask/FastAPI** - REST API framework
- **Python 3.9+** - Core language
- **Scikit-learn** - ML predictions
- **Pandas** - Data processing
- **SQLite** - Local database

### ML Model
- **Random Forest Regressor** - Carbon prediction model
- **Feature Engineering** - GPU, region, model type encoders
- **Training Dataset** - Historical ML workload data

### Deployment
- **Vercel** - Frontend hosting
- **Railway/Render** - Backend API hosting
- **GitHub Actions** - CI/CD pipeline

---

## 📁 Project Structure

```
GREENML-OPTIMIZER/
├── api-server/                 # Backend API
│   ├── main.py                # Flask/FastAPI application
│   ├── predict.py             # ML prediction logic
│   ├── database.py            # Database operations
│   ├── carbon_model.pkl       # Trained ML model
│   ├── requirements.txt       # Python dependencies
│   └── ...
├── ml-model/                   # ML training notebooks
│   ├── carbon_predictor.ipynb # Model training
│   └── ...
├── web-dashboard/              # React frontend
│   ├── public/
│   ├── src/
│   │   ├── components/
│   │   │   ├── CarbonCalculator.js
│   │   │   ├── Dashboard.js
│   │   │   ├── Header.js
│   │   │   ├── Footer.js
│   │   │   ├── Hero.js
│   │   │   └── WorkloadCreator.js
│   │   ├── services/
│   │   │   └── api.js
│   │   ├── App.js
│   │   └── index.js
│   ├── package.json
│   └── ...
├── .gitignore
├── vercel.json                 # Vercel configuration
└── README.md
```

---

## 📦 Installation

### Prerequisites

- **Node.js** 16+ and npm
- **Python** 3.9+
- **Git**

### Frontend Setup

```bash
# Clone the repository
git clone https://github.com/yourusername/greenml-optimizer.git
cd greenml-optimizer/web-dashboard

# Install dependencies
npm install

# Start development server
npm start
```

The app will open at `http://localhost:3000`

### Backend Setup

```bash
# Navigate to API server
cd api-server

# Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Run the server
python main.py
```

The API will run at `http://localhost:5000`

---

## 🎯 Usage

### 1. Calculate Carbon Emissions

Navigate to the **Carbon Calculator** and input:
- GPU Type (e.g., V100, A100, T4)
- Training Duration
- Region (for carbon intensity)
- Model Type

Click **Calculate** to get instant predictions.

### 2. Create Workload

Use the **Workload Creator** to:
- Define ML training configurations
- Compare different setups
- Optimize for carbon or cost

### 3. View Dashboard

Monitor your impact on the **Dashboard**:
- Total carbon saved
- Cost reduction
- Historical trends
- Job completion rates

---

## 🔌 API Documentation

### Base URL
```
http://localhost:5000/api
```

### Endpoints

#### POST `/predict`
Predict carbon emissions for a workload.

**Request Body:**
```json
{
  "gpu_type": "V100",
  "duration_hours": 24,
  "region": "us-east-1",
  "model_type": "transformer",
  "batch_size": 32
}
```

**Response:**
```json
{
  "carbon_emissions_kg": 45.2,
  "cost_usd": 120.50,
  "optimization_score": 85,
  "recommendations": [...]
}
```

#### GET `/jobs`
Retrieve all saved jobs.

**Response:**
```json
{
  "jobs": [
    {
      "id": 1,
      "name": "BERT Training",
      "carbon_kg": 45.2,
      "created_at": "2025-10-31T12:00:00Z"
    }
  ]
}
```

---

## 🚀 Deployment

### Deploy Frontend to Vercel

```bash
# Install Vercel CLI
npm i -g vercel

# Deploy
cd web-dashboard
vercel
```

Or connect your GitHub repository at [vercel.com](https://vercel.com)

**Configuration:**
- Framework Preset: `Create React App`
- Root Directory: `web-dashboard`
- Build Command: `npm run build`
- Output Directory: `build`

### Deploy Backend to Railway

1. Push your code to GitHub
2. Go to [railway.app](https://railway.app)
3. Create new project from GitHub repo
4. Select `api-server` directory
5. Add environment variables
6. Deploy!

---

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. **Fork** the repository
2. **Create** a feature branch (`git checkout -b feature/AmazingFeature`)
3. **Commit** your changes (`git commit -m 'Add some AmazingFeature'`)
4. **Push** to the branch (`git push origin feature/AmazingFeature`)
5. **Open** a Pull Request

### Development Guidelines

- Follow existing code style
- Write meaningful commit messages
- Add tests for new features
- Update documentation

---

## 📄 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

---

## 📧 Contact

**Aditya Choudhuri**

- GitHub: [@AdityaC-07](https://github.com/AdityaC-07)
- Email: aditya.choudhuri@somaiya.edu
- LinkedIn: [Aditya Choudhuri](https://linkedin.com/in/aditya-choudhuri-87a2a034a)

**Project Link:** [https://github.com/AdityaC-07/greenml-optimizer](https://github.com/AdityaC-07/greenml-optimizer)

---

## 🙏 Acknowledgments

- Inspired by the need for sustainable AI development
- Carbon intensity data from [Electricity Maps](https://www.electricitymaps.com/)
- ML community for open-source contributions
- All contributors and supporters

---

<div align="center">

### ⭐ Star this repo if you find it helpful!

Made with 💚 for a sustainable future

</div>
