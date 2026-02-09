# 💊 DoseGuardian – Intelligent Pill-Taking Assistant

DoseGuardian is an embedded-system–based intelligent medication reminder and monitoring system. It is designed to help patients—especially elderly people and those under long-term treatment—take their prescribed medicines on time and avoid missed doses.

---

## 🧠 Problem Statement
Many patients forget or skip their medication schedules, which can lead to serious health complications and reduced treatment effectiveness. DoseGuardian solves this problem by using a microcontroller-based reminder system with real-time alerts and user acknowledgment.

---

## 🎯 Aim
To design and implement an intelligent pill-taking assistant that reminds users to take medicines at scheduled times and monitors whether the dose was taken or missed.

---

## ✅ Objectives
- Display real-time date and time using RTC on LCD  
- Allow users to modify RTC settings using a 4×4 keypad  
- Enable users to set medicine schedules  
- Trigger alerts when medicine time matches the current time  
- Indicate missed doses using LED  

---

## 🧩 System Components

### 🔧 Hardware Requirements
- LPC2148 Microcontroller  
- 16×2 LCD  
- 4×4 Matrix Keypad  
- RTC  
- Buzzer  
- Switches  
- LED  
- USB-UART Converter / DB-9 Cable  

### 💻 Software Requirements
- Embedded C  
- Flash Magic  

---

## ⚙️ Working Principle

### 1️⃣ Setting the Medicine Schedule
- User presses **Switch 1**
- Medicine time is entered via keypad
- Schedule is stored in microcontroller memory
- LCD displays stored medicine time along with RTC info

### 2️⃣ Real-Time Monitoring
- Microcontroller continuously checks RTC time
- Compares current time with stored medicine schedule

### 3️⃣ Alert Mechanism
- LCD displays message like **“TAKE MEDICINE NOW”**
- Buzzer turns ON and OFF at fixed intervals

### 4️⃣ User Acknowledgment
- User presses **Switch 2** to confirm medicine intake
- If not acknowledged within a given time:
  - **Red LED turns ON**, indicating a missed dose

---

## 🧭 Software Flow
1. Initialize RTC, LCD, Keypad, and Buzzer  
2. Display current date and time  
3. Accept medicine schedule input when Switch 1 is pressed  
4. Continuously monitor RTC  
5. Trigger alert when schedule matches  
6. Wait for user acknowledgment  
7. Restart monitoring after acknowledgment  
8. Turn ON red LED if acknowledgment is missed  

---

## 📋 Menu Options

### Main Menu
