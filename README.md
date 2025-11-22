# AI-KYC-Application

## Project Overview

The AI-KYC Automation Platform is an advanced, real-time video KYC solution designed to replace manual, cumbersome, and non-inclusive customer onboarding processes. Leveraging state-of-the-art AI and machine learning, this platform ensures a seamless, highly secure, and compliant digital identity verification experience.

**Problem:** Traditional KYC processes are slow, expensive, prone to human error, and create significant customer friction.

**Our Solution:** An AI-driven conversational flow that automates identity verification using facial authentication, document OCR, and voice confirmation, reducing onboarding time from days to minutes.

## Key Features

* **AI-driven Conversational Flow:** Guides the user step-by-step through the verification process without human intervention.
* **Facial Authentication:** Real-time liveness detection and identity matching against document photos.
* **Document Verification:** Automated OCR (Optical Character Recognition) for instant data extraction from PAN/Aadhaar cards.
* **Signature Verification:** ML model to analyze and verify captured signatures.
* **Accessibility & Compliance:** **Read-aloud Details with Voice Confirmation** using Text-to-Speech (TTS) and Speech-to-Text (STT) for explicit user consent and inclusivity.
* **Secure Session Control:** **Browser/tab locking** during the live KYC process to prevent fraud and maintain session integrity.
* **Agent Support:** Seamless escalation path for human agent intervention when necessary.

---

## Technology Stack

Our platform utilizes a robust and modern stack for performance and scalability:

| Component | Technologies Used | Rationale |
| :--- | :--- | :--- |
| **Frontend** | **Next.js**, **Shadcn** | High-performance UI, Server-Side Rendering (SSR) for fast loading. |
| **Real-Time Video** | **WebRTC** | Low-latency, peer-to-peer live video streaming essential for V-KYC. |
| **Backend API** | **Node.js (Express.js)**, **TypeScript** | High concurrency handling, robust routing, and type safety for the API Gateway. |
| **ML Services** | **Python (Flask)** | Dedicated, high-performance microservices for ML inference. |
| **Database** | **MongoDB** | Flexible NoSQL storage for structured user data and unstructured verification logs. |
| **AI/ML Libraries**| **Deepface**, **VGG 19**, **Opencv**, **pytesseract** | Core models for recognition, liveness, and OCR. |
| **Conversational AI**| **Bark AI**, **Whisper AI** | Text-to-Speech (TTS) and Speech-to-Text (STT) for audio compliance. |

---

## System Architecture

The platform operates on a **Microservices Architecture** to ensure reliability, independent deployment, and scalable performance.

1.  **Client Layer (Next.js/WebRTC):** Handles user interaction and streams encrypted video/audio to the backend.
2.  **API Gateway (Node.js/Express.js):** Orchestrates all requests, handles security checks, and routes traffic.
3.  **ML Verification Microservices (Python/Flask):** Decoupled services dedicated to high-speed computation for:
    * Facial Liveness and Authentication (VGG 19, Deepface).
    * Document OCR and validation (pytesseract, OpenCV).
4.  **Database Layer (MongoDB):** Stores all user profiles and the immutable audit trail of every KYC session, enabling horizontal scalability via sharding.
<img width="1484" height="1038" alt="image" src="https://github.com/user-attachments/assets/3866ca31-7deb-4daa-833b-1ee2d6d87dfa" />

---

## AI / ML Components in Detail

| Component | Technology Used | Function and Regulatory Relevance |
| :--- | :--- | :--- |
| **Facial Recognition** | **VGG 19** / **Deepface** | Verifies the live user against the ID photo. Used for mandatory identity proofing. |
| **Liveness Detection** | **OpenCV** & Movement Analysis | Prevents spoofing (using photos or recorded video) by detecting subtle human movements. |
| **Document OCR** | **pytesseract** | Extracts text from ID documents to populate forms automatically, reducing human data entry errors. |
| **Voice Confirmation** | **Bark** (TTS) and **Whisper AI** (STT) | Reads key details back to the user, who confirms verbally. The STT output is stored for irrefutable proof of consent and compliance. |
| **Image Pre-processing** | **OpenCV** / **cascade classifier** | Optimizes captured images (deskewing, cropping) to ensure high accuracy for the downstream ML models. |

---

## Security and Compliance

Security is embedded into the core design to handle sensitive PII (Personally Identifiable Information).

* **Encryption:** **TLS/SSL (HTTPS/WSS)** for data in transit (APIs and WebRTC streams) and AES-256 for data at rest (MongoDB).
* **Fraud Mitigation:** Automated liveness detection and enforced **browser/tab locking** during the session.
* **Audit Trail:** Every step, including ML scores and voice confirmation transcriptions, is logged in an immutable record in MongoDB for regulatory compliance (KYC/AML).

---

## Scalability and Performance

The architecture is built for high availability and elastic scalability, critical for a platform expected to handle peak onboarding demands.

* **Elastic Scaling:** Stateless APIs and ML services are designed for containerization (e.g., Docker/Kubernetes), allowing instant horizontal scaling under heavy load.
* **Real-Time Efficiency:** **WebRTC** minimizes server load, and dedicated **Python/Flask** ML microservices ensure rapid inference times (low latency) for facial authentication.
* **Database Scalability:** MongoDB supports horizontal sharding, ensuring the database can handle increasing data volume without performance degradation.

---

## Getting Started

Instructions on setting up and running the project locally.

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/LabhanshiBhatia/AI-KYC-Application](https://github.com/LabhanshiBhatia/AI-KYC-Application)
    cd AI-KYC-Application
    ```
2.  **Install dependencies:** (Instructions for Frontend, Backend, and ML services)
    ```bash
    # Example: Install frontend dependencies
    cd client
    npm install
    # Example: Install backend/ML dependencies
    cd server/ml_service
    pip install -r requirements.txt
    ```
3.  **Configure Environment:** Set up your MongoDB connection strings and required API keys in the `.env` files.
4.  **Run Services:**
    ```bash
    # Command to start all required services (Frontend, API Gateway, ML Services)
    # Example: npm start (or a script to run services via Docker Compose)
    ```

---

## Live Demo and Submission Links

| Item | Status | Link |
| :--- | :--- | :--- |
| **Code Repository** | Active | `https://github.com/LabhanshiBhatia/AI-KYC-Application` |
| **Live Prototype Demo**| **[To be Inserted]** | **[Link to YouTube, Vimeo, or Google Drive Video]** |
| **Round 2 Submission PDF**| **[Pending]** | *(Link to the final submitted document)* |

---

## Team Members

| Name | Role |
| :--- | :--- |
| **Labhanshi Bhatia** | **ML and Backend Developer** |
| **Lavanya Yadav** | **Full Stack Developer** |
| **KM Yogita** | **ML and Backend Developer** |
| **Kanika** | **Full Stack Developer** |

---
