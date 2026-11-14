<p align="center">
  <img src="assets/banner.png" alt="PEKKA-AI Banner" width="100%">
</p>

# ◈ PEKKA AI

## ◆ About the Project
PEKKA AI is an autonomous decision-support system designed for monitoring critical electrical infrastructure with a focus on power grid transformers. It continuously processes 18 real-time sensor streams to detect operational anomalies, predict potential component failures, and calculate risk scores. The platform functions strictly as a human-in-the-loop decision-support tool, providing preventive recommendations while leaving operational switching decisions to qualified operators.

## ❖ Key Features
- Ingestion pipeline for 18 live telemetry streams including top-oil temperature, winding temperature, vibration, and dissolved gas analysis (DGA).
- Dual-layer anomaly detection utilizing rule-based physical safety limit validation and an Isolation Forest machine learning model.
- Predictive failure classification engine powered by a Random Forest algorithm.
- 0 to 100 composite operational disruption risk scoring engine.
- Interactive operator web dashboard displaying telemetry charts, warning levels, and operational recommendations.
- Java-based telemetry simulation harness for reproducible stress testing across normal, warning, and critical scenarios.

## ⬢ Technologies Used
- Python 3.10+
- FastAPI
- Scikit-Learn
- Pandas & NumPy
- Java 17+ (Spring Boot Simulator)
- React 18
- Vite
- Tailwind CSS

## § Requirements
- Python 3.10 or higher
- Java Development Kit (JDK) 17 or higher
- Node.js 18 or higher

## ▲ Installation & Execution
```bash
# 1. Run Backend
cd backend
python -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate
pip install -r requirements.txt
uvicorn main:app --reload --port 8001

# 2. Run Java Simulator
cd ../simulator
mvn clean test-compile
mvn exec:java -Dexec.mainClass="com.pekka.simulator.SimulatorApplication"

# 3. Run Frontend
cd ../frontend/pekka-ai
npm install
npm run dev
```

## ※ Developer
Developer: ISBANDU RAHUMAN R  
GitHub: https://github.com/ISBANDURAHUMAN-R
