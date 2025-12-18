Smart Sign Language Glove 🧤

A real-time gesture recognition system that translates sign language into text using an ESP32, Flex Sensors, and Machine Learning.

📌 Project Overview

This project consists of three main parts working together:

Hardware (The Hand): An ESP32 reads 5 flex sensors (fingers) and an MPU6050 gyroscope (wrist orientation).

Backend (The Brain): A Python script collects data, trains a Random Forest AI model, and serves predictions via WebSocket.

Frontend (The Interface): A React dashboard visualizes the sensor data and displays the predicted letter in real-time.

📂 Repository Structure

├── firmware/          # ESP32 C++ Code (Arduino IDE)
├── backend/           # Python AI & Server scripts
│   ├── collect_data.py
│   ├── train_model.py
│   ├── server.py
│   └── gesture_data.csv
├── frontend/          # React Web Application
└── README.md


🔌 Hardware Connections

Finger

ESP32 Pin

Thumb

GPIO 32

Index

GPIO 35

Middle

GPIO 34

Ring

GPIO 39 (SN)

Pinky

GPIO 36 (SP)

Note: All flex sensors use a voltage divider circuit with a 10kΩ resistor.

🚀 Getting Started

1. Firmware Setup

Open the code in firmware/ using Arduino IDE.

Install the Adafruit MPU6050 library.

Upload to your ESP32.

2. Backend Setup (Python)

Navigate to the backend folder and install dependencies:

pip install pyserial pandas scikit-learn joblib websockets numpy


Workflow:

Run python collect_data.py to record your hand gestures.

Run python train_model.py to generate the AI brain (.pkl file).

Run python server.py to start the WebSocket bridge.

3. Frontend Setup (React)

Navigate to the frontend folder:

npm install
npm run dev


📸 Usage

Plug in the Glove (ESP32).

Start the Python Server.

Open the React Web App.

Click Connect and start signing!

Created for the Smart Gloves Project.
