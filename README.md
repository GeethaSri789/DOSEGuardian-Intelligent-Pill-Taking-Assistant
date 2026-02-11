# 💊 Dose Guardian – Intelligent Pill-Taking Assistant

Dose Guardian is an embedded-system–based intelligent medication reminder and monitoring system. It is designed to help patients—especially elderly people and those under long-term treatment—take their prescribed medicines on time and avoid missed doses.

---

## 🧠 Problem Statement
Many patients forget or skip their medication schedules, which can lead to serious health complications and reduced treatment effectiveness. Dose Guardian solves this problem by using a microcontroller-based reminder system with real-time alerts and user acknowledgment.

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

## 📸LCD Display

### Full Proteus Setup
![WhatsApp Image 2026-02-09 at 11 09 11 PM](https://github.com/user-attachments/assets/160c0fee-2947-4cfc-ad0f-5495c2e1e473)

---

### ⌚ Main Menu
![WhatsApp Image 2026-02-09 at 11 08 52 PM](https://github.com/user-attachments/assets/b941c5e3-92dd-4f01-bece-904d1f98ec1b)

---

### ✏️ Editing Time & Set Medicine Time
- Right ( > ) → Move between HH • MM • SS
- Left ( < ) → Move backward
- ↑ → Increase value
- ↓ → Decrease value

![WhatsApp Image 2026-02-09 at 11 08 56 PM](https://github.com/user-attachments/assets/7c36803c-2c52-4d28-81f9-cd4af6e576e3)

---

### 💊 Medicine Time
![WhatsApp Image 2026-02-09 at 11 09 27 PM](https://github.com/user-attachments/assets/f9431a99-abdc-4a95-933a-84ad2dba80b0)

- LCD shows TIME FOR MEDICINE
- Buzzer turns ON 🔔

---

## ⏰ Switch Pressed
![WhatsApp Image 2026-02-09 at 11 09 40 PM](https://github.com/user-attachments/assets/d6880e4a-f6eb-4aeb-b699-0bce9e66ad69)

- When Switch is press within medicine time
- Buzzer turn OFF 🔕
- Green LED glows for attention 💡

---

## ⌛ Switch Not Pressed

![WhatsApp Image 2026-02-09 at 11 09 48 PM](https://github.com/user-attachments/assets/67f2ddc8-dd4a-44ba-a5db-85c95e8c2a5b)

- When Switch is not pressed within time
- Buzzer turn OFF 🔕
- Red LED glows for attention 💡
  
---

## 🔑Keypad Controls
| Key         | Function                  |
| ----------- | ------------------------- |
| `A`         | Move selection forward    |
| `B`         | Move selection backward   | 
| `C`         | Decrement value           | 
| `D`         | Increment value           |             
| `=`         | Save / Confirm            |

---

## 🧭 User Guide
1. Power on the system — the LCD shows Date & Time.
2. Press the configured menu switch to enter settings.
3. Use the keypad to edit:
    * RTC Time (HH:MM:SS)
    * RTC Date (DD/MM/YYYY)
    * Device ON Time
    * Device OFF Time
4. Navigation controls:
    * “>” → Move Right
    * “<” → Move Left
    * ↑ → Increment
    * ↓ → Decrement
5. Confirm inputs — invalid entries trigger warnings.
6. Exit to return to normal running mode with updated parameters.

---

## 💡Future Enhancements
- Multiple medicine schedules
- EEPROM or Flash memory storage
- GSM or SMS alert system
- Mobile application integration
- Voice reminders
- Low-power sleep mode

---

## 👤Developed By
**P.V.Geetha Sri**  
Electronics and Communication Engineering  
Developer of DoseGuardian – *Intelligent Pill-Taking Assistant*

---

## 📜License
This project is developed for academic and learning purposes. You are free to modify and enhance it with proper credit.  
⭐ If you find this project useful, consider giving it a star on GitHub.
