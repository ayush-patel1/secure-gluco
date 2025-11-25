

---

# 🛡️ SecureGluco — AI-Driven Security & Glucose Monitoring Platform

SecureGluco is a unified platform that combines **real-time glucose monitoring**, **insulin pump telemetry**, and an **AI-powered Intrusion Detection System (IDS)** designed specifically for BioMEMS and IoMT medical devices.
It provides clinicians and patients with a secure, intelligent, and reliable ecosystem for diabetes care while protecting insulin pumps and CGMs against cyber threats.

---

## 📘 1. Overview

Modern IoMT medical devices—particularly **insulin pumps** and **continuous glucose monitors (CGMs)**—are increasingly connected and therefore increasingly vulnerable. Cyberattacks can manipulate dosage, spoof health readings, or disrupt communication, posing severe risks to patient safety.

SecureGluco addresses these challenges through:

* 🩺 **Real-time glucose & insulin telemetry**
* 🔐 **AI-driven anomaly detection** for securing insulin pumps and CGMs
* 📡 **Live monitoring of IoMT device traffic**
* 🧭 **Digital Twin–based deviation detection**
* 📊 **Interactive clinical dashboard for synchronized health + security insights**

The system provides end-to-end protection with sub-second detection, advanced AI models, and secure communication channels.

---

## 🚨 2. Problem Statement

Connected medical devices face growing security challenges:

### ❌ Limitations of Current Systems

* No lightweight IDS optimized for IoMT compute constraints
* Legacy wireless protocols vulnerable to spoofing
* Insufficient real-time detection capabilities
* General-purpose antivirus/IDS tools unsuitable for embedded medical systems

### ⚠️ Impact & Risks

* Incorrect insulin delivery → dangerous hypo/hyperglycemia
* Data theft or manipulation
* Remote device takeover
* Disrupted communication during emergencies

SecureGluco provides a medical-grade protective layer built around privacy, reliability, and rapid detection.

---

## 🎯 3. System Objectives

SecureGluco aims to:

* Detect cyber threats to insulin pumps within **<500ms**
* Offer a **unified dashboard** combining glucose trends and security alerts
* Apply **AES-256 encryption** and **multi-factor authentication**
* Deploy **lightweight AI models** suitable for embedded or low-power devices
* Monitor **network-level telemetry** from IoMT devices
* Employ **Digital Twins** to identify deviations in pump or CGM behavior
* Maintain interoperability with modern diabetes care systems

---

## 🧠 4. AI Model — ANN + LSTM + Attention

The SecureGluco IDS is powered by a hybrid deep learning model:

### ✔ Artificial Neural Network (ANN)

Captures **spatial** properties:

* Packet-level anomalies
* Protocol misuse
* Abnormal HTTP/TCP metadata

### ✔ Long Short-Term Memory (LSTM)

Learns **temporal** patterns:

* Attack sequences
* DDoS bursts
* Unexpected rate fluctuations

### ✔ Attention Mechanism

* Highlights dominant features
* Improves interpretability for clinical & security analysis

### 📈 Key Metrics

* **Accuracy:** 97–99%
* **False Alarms:** <1%
* **Zero-day Detection TPR:** 0.89
* **Model Size Reduction:** 34× using quantization


## 📡 6. System Workflow

### **1. IoMT Network Traffic Collection**

Glucose monitors, insulin pumps, and wearables send telemetry and network packets.

### **2. Preprocessing Module**

* Cleans and normalizes packets
* Extracts HTTP and TCP features
* Generates session-level metrics

### **3. Feature Extraction**

* TCP header/flag analysis
* Session rate analysis
* HTTP metadata extraction

### **4. AI Prediction Engine**

The ANN–LSTM–Attention model:

* Classifies normal vs. malicious traffic
* Detects spoofing, flooding, replay, and injection attacks
* Produces confidence scores

### **5. Visualization Layer**

The dashboard displays:

* Real-time glucose levels
* Insulin delivery patterns
* Live threat indicators
* Anomaly explanations

### **6. Security Recommendation Engine**

Generates automated suggestions:

* Device isolation
* Alerting clinicians
* Blocking malicious traffic
* Re-calibrating device behavior

---

## 🖥️ 7. Tech Stack

### **Frontend**

* Next.js + React + TypeScript
* Tailwind CSS for fast, responsive UI
* D3.js for analytics visualizations
* Streamlit for model introspection views

### **Backend**

* Node.js + Express REST APIs
* Python ML service (PyTorch + TensorFlow Lite)
* Next.js serverless API routes

### **AI / ML**

* ANN–LSTM–Attention hybrid
* TFLite quantized model
* Federated Learning support
* Digital Twin behavior simulation

### **Database**

* PostgreSQL / TimescaleDB (time-series optimized)

### **Security**

* AES-256-GCM
* JWT-based authentication
* Multi-Factor Authentication
* Zero-Trust Access Control

---

## 📊 8. Results Summary

* **97–99% detection accuracy** across multiclass IoMT threats
* **<0.10% false positive rate**
* **<500ms inference latency** for real-time protection
* **Zero-Day threat recall of 0.89**
* **4× reduced communication overhead** via model optimization
* Adaptive learning boosts accuracy from **72% → 90%** during Digital Twin re-training cycles

---

## 📱 9. Live Platforms

| Component                  | Link                                                                           |
| -------------------------- | ------------------------------------------------------------------------------ |
| **Web Dashboard**          | [https://secure-gluco.vercel.app/](https://secure-gluco.vercel.app/)           |
| **Model Demo (Streamlit)** | [https://modelbackendai.streamlit.app/](https://modelbackendai.streamlit.app/) |

---

## 🧪 10. Local Setup

```bash
git clone https://github.com/ayush-patel1/secure-gluco.git
cd secure-gluco

pnpm install
cp .env.example .env.local

pnpm dev
```

### **Required Environment Variables**

* `DATABASE_URL`
* `NEXTAUTH_URL`
* `NEXTAUTH_SECRET`
* `MODEL_API_URL` (Python inference service)

---

## 🧩 11. Folder Structure

```
/secure-gluco
 ├── app/                 # Next.js routes & pages
 ├── components/          # UI components
 ├── lib/                 # Utilities & helpers
 ├── prisma/              # Database schema (Prisma)
 ├── public/              # Static assets
 ├── model-service/       # Python ANN–LSTM model engine
 └── README.md
```

---

## 🏁 12. Conclusion

SecureGluco delivers a unique convergence of **health monitoring**, **cybersecurity**, and **AI**, offering:

* Real-time clinical telemetry
* Medical-grade cybersecurity
* Lightweight AI models for IoMT devices
* High interpretability and strong zero-day defenses
* Unified dashboard for clinicians and patients

It is designed to enhance safety, trust, and reliability in next-generation diabetes care.

---

