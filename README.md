# SmartAgri

**11th Huawei ICT Competition – Innovation Track (Asia Pacific)**  
**Team:** FroiCaDen | **University:** De La Salle University

---

## 📖 Project Overview
Plant diseases destroy 20% to 40% of global crop yields annually, disproportionately affecting rural smallholder farmers who lack access to professional agronomists. **SmartAgri WebBot** is a lightweight, browser-based Progressive Web App (PWA) that enables farmers to snap a photo of a diseased crop leaf using their smartphone camera and instantly receive an AI-powered diagnosis along with affordable, localized treatment recommendations.

By offloading all heavy computation to **Huawei Cloud**, the platform requires zero custom hardware and runs smoothly on low-storage mobile devices over standard cellular networks.

---

## ✨ Key Features
* **Zero-Install Mobile Web Interface:** Uses HTML5 native camera capture so farmers can diagnose crops directly from their mobile browser without downloading heavy apps.
* **Real-Time AI Disease Detection:** Identifies 15+ common crop diseases with **94.5% validation accuracy** in under 2.5 seconds.
* **Actionable Treatment Guides:** Translates AI predictions into step-by-step, low-cost agricultural remedies.
* **Outbreak Logging & Analytics:** Tracks diagnosis history and regional disease trends via cloud database logging.

---

## ☁️ Huawei Cloud Technology Stack
* **Compute & Web Hosting:** Huawei Elastic Cloud Server (ECS) running Ubuntu, Nginx, and Python (Flask).
* **AI Training & Inference:** Huawei ModelArts & MindSpore (Convolutional Neural Network trained on the PlantVillage dataset and deployed as a Real-Time Service API).
* **Object Storage:** Huawei Object Storage Service (OBS) for storing the 50,000+ training images and handling temporary image uploads.
* **Database:** Huawei Relational Database Service (RDS for MySQL) for logging diagnosis timestamps, confidence scores, and crop trends.

---

## 📂 Repository Structure
```text
SmartAgri-WebBot/
├── backend/                # Python Flask API & Huawei ModelArts integration
│   ├── app.py              # Main server routing and RDS logging
│   └── requirements.txt    # Python dependencies
├── frontend/               # Mobile-responsive HTML5/CSS/JS web interface
│   ├── index.html          # Camera upload UI & results display
│   └── app.js              # Fetch API logic for image submission
├── model/                  # MindSpore training scripts & dataset config
└── README.md               # Project documentation
```

---

## 🚀 Quick Start (Local Testing)
*(Note: Currently in preliminary prototype phase; full ECS deployment will follow regional qualification.)*

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/](https://github.com/)[YourUsername]/SmartAgri-WebBot.git
   cd SmartAgri-WebBot/backend
   ```
2. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```
3. **Configure environment variables:**
   Add your Huawei Cloud `X-Auth-Token`, ModelArts Endpoint URL, and RDS credentials in a `.env` file.
4. **Run the Flask server:**
   ```bash
   python app.py
   ```

---

## 👥 Team Members & Roles
| Name | Role | Responsibilities |
| :--- | :--- | :--- |
| **Denise Verzosa]** | AI & Data Lead | Dataset preparation in Huawei OBS; model training & deployment on ModelArts. |
| **Froilene Villaluz** | Cloud Backend Architect | Huawei ECS configuration, Flask REST API, and Huawei RDS database integration. |
| **Catherine Xu** | Frontend & UI/UX Developer | Mobile-responsive web interface, HTML5 camera integration, and user testing. |
| **Jared Abayan** | Project Advisor | Technical architecture review, quality assurance, and competition guidance. |
