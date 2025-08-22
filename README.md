# Driver Sleep Detection and Emergency Alert System 🚗💤

This project detects driver drowsiness using computer vision techniques and triggers an alert (buzzer) to prevent accidents.

---

## 👨‍💻 About Me
**Name:** Ardeepan S  
**DOB:** 10-03-2005  
**Degree:** B.E. Electronics and Communication Engineering  
**College:** V.S.B. College of Engineering Technical Campus, Coimbatore  

**Career Objective:**  
As an aspiring engineering student, I seek a role to apply my technical knowledge and to develop my skills. I am eager to contribute my problem-solving abilities, enthusiasm, and strong work ethic to innovative projects.

---

## 📚 Educational Qualification
- **B.E / ECE** – Pursuing, V.S.B. College of Engineering Technical Campus  
- **HSC** – Pursuing, Govt. Hr. Sec. School, Udaiyarpalaiyam  
- **SSLC (2022)** – Govt. Hr. Sec. School, Udaiyarpalaiyam  

---

## 💡 Technical Skills
- Programming: **Java, C**
- Tools/Domain: Embedded Systems, IoT, Cloud Computing, Industry 4.0  

---

## 🌟 Soft Skills
- Leadership & Time Management  
- Critical Thinking  
- Adaptability  
- Teamwork & Collaboration  

---

## 🏆 Patents
1. **A Secure iBeacon Ecosystem for Women's Safety with Real-Time Threat Detection in IoT Communication** – 202541027524 A (25/04/2025)  
2. **Smart Water Management Future Research and Survey Detection** – 202541038028 A (16/05/2025)  

---

## 🛠 Projects
- LED Arcade Game  
- Driver Sleep Detection and Emergency Alert System  
- IoT Smart Parking Using RFID Scan and Parking Slot Availability  
- Smart Industrial Monitoring System (Internship Project)  

---

## 📜 Certifications
- Internship – **Zekatix** (Embedded Systems & IoT) – 2023  
- **NPTEL (Elite):** IoT (2024), Industry 4.0 (2025), Cloud Computing (2025)  
- Internship – **Emglitz Technologies** (Embedded Systems) – 2025  
- TCS CodeVita XII Global Rank: **4395** (2025)  

---

## 🚀 Driver Sleep Detection Code Example

```python
import cv2
import dlib
from scipy.spatial import distance as dist

# Function to calculate Eye Aspect Ratio (EAR)
def eye_aspect_ratio(eye):
    A = dist.euclidean(eye[1], eye[5])
    B = dist.euclidean(eye[2], eye[4])
    C = dist.euclidean(eye[0], eye[3])
    return (A + B) / (2.0 * C)

EYE_AR_THRESH = 0.25
EYE_AR_CONSEC_FRAMES = 20

print("🚗 Driver Drowsiness Detection Started... Stay Awake!")
