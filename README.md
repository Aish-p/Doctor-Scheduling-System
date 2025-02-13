# Online Medical Appointment System

## 🎯 Project Aim

Simulation of an online medical appointment system using a hybrid architecture of TCP and UDP sockets.

## 📜 Project Description

We have the health center server for authenticating users and reserving time slots, 2 patients and 2 doctors. Communication between the health center server and patients in the first 2 phases is through TCP sockets. In the last phase, communication between the doctors and the patients is through UDP sockets.

**The program runs in three phases:**

1. **User Authentication** – Patients authenticate with the Health Center Server via TCP.
   
    In the first phase, patients connect with the health center server on a static port using TCP socket. On successful authentication by the server, they can continue to phase 2 and ask for available time slots      for appointment.

2. **Scheduling an Appointment** – Patients request and reserve available time slots.

    In the second phase, the server will send a list of available time slots to the patient. The patient chooses one time slot and, if that has not already been reserved, that slot is reserved for the asking 
    patient. The server sends doctor's port number, associated with that time slot, on which the patient will now connect in phase 3.

3. **Estimated Cost Calculation** – Patients communicate with doctors via UDP for cost estimation.

    In the third phase, the patient sets up a Bidirectional UDP connection with the stipulated doctor on the received doctor port number. The patient sends his insurance information to the doctor, who replies on      the same UDP port with the estimated cost of the visit related to that insurance.

   
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

## 📂 Files & Descriptions

| File | Description |
|------|------------|
| `healthcenterserver.py` | This is the code for the health center server. It reads the username and password information of authentic users from users.txt and the availabilities, doctors's information from availabilities.txt. It is responsible for authenticating the patients, scheduling appointments and sending doctors's information to them. |
| `doctor1.py` | This is the code for Doctor 1. It reads Insurance information from `doc1.txt` and sends the estimated cost of visit associated with each insurance type to the patients. |
| `doctor2.py` | This is the code for Doctor 2. It reads Insurance information from `doc2.txt` and sends the estimated cost of visit associated with each insurance type to the patients. |
| `patient1.py` | This is the code for Patient 1. It reads username and password of patient 1 from `patient1.txt` and the type of insurance from `patient1insurance.txt`. It communicates with the health center server on a dynamic TCP port and with the doctors on a dynamic UDP port. |
| `patient2.py` | This is the code for Patient 2. It reads username and password of patient 2 from `patient2.txt` and the type of insurance from `patient2insurance.txt`. It communicates with the health center server on a dynamic TCP port and with the doctors on a dynamic UDP port. |


💡 Tip: Ensure all required text files are present before running the scripts.

📌 Enjoy the simulation of an online medical appointment system! 😊

