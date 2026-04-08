# Face-and-liveliness-detection-based-bank-locker-ML
face Recognition and Liveness Detection Based Bank Locker System -  This project implements a secure bank locker access system using Face Recognition  combined with Liveness Detection to prevent spoofing attacks such as photo or video fraud.  
🔐 Face Recognition & Liveness Detection Based Bank Locker System

📌 Project Overview

This project presents a secure bank locker access system that integrates face recognition with liveness detection (eye blink verification) to ensure that only an authorized and physically present user can access the locker.

Traditional biometric systems are vulnerable to spoofing attacks using photos, videos, or masks. To address this limitation, the system introduces a real-time liveness check, making it more robust and reliable for high-security environments such as bank lockers.

🎯 Objectives
  To develop a contactless and secure authentication system
  To prevent spoofing attacks using static images or recorded videos
  To implement real-time face recognition with liveness validation
  To simulate secure locker access control
      🚀 Key Features
      
  1. Real-Time Face Detection
Detects human faces from a live webcam feed
Uses Haar Cascade classifier for efficient detection
Works under varying lighting conditions (with some limitations)
  2. Face Recognition
Compares detected face with pre-stored authorized user image
Uses encoding-based matching for accuracy
Provides quick authentication results
  3. Eye Blink Based Liveness Detection
Detects eye regions using Haar Cascade
Monitors eye state (open/closed)
Requires a blink action to confirm user is live
Prevents access using photos or screen replay attacks
  4. Anti-Spoofing Mechanism
Rejects static images without eye movement
Ensures real human interaction before granting access
  5. Secure Locker Access Simulation
Grants access only when both conditions are satisfied:
Face matches authorized user
Liveness (blink) is verified
Displays access status: “Access Granted” / “Access Denied”
           🧠 Technology Stack
     
     Programming Language
Python – Core development and logic implementation
Libraries & Frameworks
OpenCV – Image processing and real-time video capture
face_recognition – Face encoding and matching
dlib – Facial landmark detection
NumPy – Array operations and calculations
Machine Learning Models
Haar Cascade Classifier (for face & eye detection)
Pre-trained face recognition model (dlib-based)
    📂 Project Structure
Face-Liveness-Bank-Locker/
│
├── face_liveness_locker.py       # Main implementation file
├── requirements.txt              # Dependencies list
├── README.md                     # Project documentation
│
├── dataset/
│   └── authorized_user.jpg       # Stored authorized user image
│
└── cascades/
    ├── haarcascade_frontalface_default.xml   # Face detection model
    └── haarcascade_eye.xml                   # Eye detection model
            ⚙️ Working Principle (Step-by-Step)
     
Video Capture Initialization
Webcam starts capturing real-time frames
Face Detection
Each frame is processed to detect faces using Haar Cascade
Face Encoding & Matching
Detected face is encoded
Compared with stored authorized user encoding
Eye Detection & Blink Monitoring
Eye regions are extracted
System checks for eye closure and reopening (blink pattern)
Liveness Verification
If blink is detected → user is considered live
If no blink → possible spoof attempt
Authentication Decision
If Face Match + Blink Verified → Access Granted
Else → Access Denied

🔒 Security Advantages

Prevents photo-based spoofing attacks
Reduces risk of video replay attacks
Provides multi-layer authentication (Face + Liveness)
Enhances security compared to traditional PIN/password systems

⚠️ Limitations

Performance may degrade in low lighting conditions
Requires clear visibility of eyes for blink detection
Limited to single authorized user (in current implementation)
Haar Cascade is less accurate compared to deep learning models

🔮 Future Enhancements

Multi-user support with database integration
Integration with Deep Learning models (CNNs) for better accuracy
Advanced liveness detection (head movement, depth sensing)
Deployment with IoT-based smart lockers
Integration with OTP or biometric multi-factor authentication
📌 Conclusion

This project demonstrates a practical implementation of a secure and intelligent locker system using computer vision techniques. By combining face recognition with liveness detection, it significantly enhances authentication reliability and reduces vulnerability to spoofing attacks, making it suitable for real-world security applications.
