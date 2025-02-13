# Online Medical Appointment System

## 🎯 Project Aim

Simulation of an online medical appointment system using a hybrid architecture of TCP and UDP sockets.

## 📜 Project Description

The program runs in three phases:

1. **User Authentication** – Patients authenticate with the Health Center Server via TCP.

2. **Scheduling an Appointment** – Patients request and reserve available time slots.

3. **Estimated Cost Calculation** – Patients communicate with doctors via UDP for cost estimation.

## 🔗 System Components

* Health Center Server 🖥️

* Two Patients 🤒🤕

* Two Doctors 👩‍⚕️👨‍⚕️

## 🔄 Communication Flow

* Phase 1 & 2: TCP communication between patients and the health center server.

* Phase 3: UDP communication between patients and doctors for cost estimation.

## ▶️ How to Run the Program

Run the processes in the following order:

1️⃣ Start the Health Center Server 🖥️:

```
python healthcenterserver.py
```

2️⃣ Start both Doctors 🏥:

```
python doctor1.py
python doctor2.py
```

3️⃣ Start both Patients 😷:

```
python patient1.py
python patient2.py
```

💡 Tip: Ensure all required text files are present before running the scripts.

📌 Enjoy the simulation of an online medical appointment system! 😊

