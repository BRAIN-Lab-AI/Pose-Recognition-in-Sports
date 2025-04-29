# 🏋️‍♂️ Squat Assessment Using Pose Estimation: A Rule-Based Framework for Fitness Applications


## 🎯Introduction

This project introduces an AI-powered **Squat Analysis System** that leverages pose estimation and deep learning techniques to evaluate squat form in real-time using video input. Built using **MediaPipe**, **OpenCV**, and **Streamlit**, it accurately tracks key body landmarks and angles to classify posture, count repetitions, and provide actionable feedback. Designed for both beginners and professionals, this system offers a seamless and intuitive interface to help athletes and fitness enthusiasts enhance their workout performance while avoiding incorrect form that may lead to injury.

[![Picture1.png](https://i.postimg.cc/k4dmJg1R/Picture1.png)](https://postimg.cc/WDSKSTPs)

## 📚Project Metadata

### 👩‍💻 Authors

- **Team:** Haya Shujaa Aldawsari
- **Supervisor Name:** Dr. Muzammil Behzad
- **Affiliations:**  King Fahd University of Petroleum and Minerals, Dhahran, Saudi Arabia

### 📄 Project Documents

- **Presentation:** [Project Presentation](https://github.com/BRAIN-Lab-AI/Pose-Recognition-in-Sports/blob/main/Squat%20Assessment%20Using%20Pose%20Estimation.pptx)
- **Report:** [Project Report](https://github.com/BRAIN-Lab-AI/Pose-Recognition-in-Sports/blob/main/Squat%20Assessment%20Using%20Pose%20Estimation%20Report.pdf)


### 📚 Reference Paper

- [BlazePose: On-device Real-time Body Pose Tracking](https://arxiv.org/abs/2006.10204)



## 🛠️ Project Technicalities

### Terminologies

- **Pose Estimation:** Technique to locate key human joints in images or video.
- **MediaPipe:** A framework by Google for building pipelines to process video, audio, and other multimedia.
- **Hip-Knee-Ankle Angle:** Used to assess depth and form during squats.
- **Offset Angle:** Measures camera alignment based on the nose-shoulder angle.
- **Inactivity Detection:** Mechanism to reset counters if no movement is detected for a defined time.
- **Squat States:** s1 (standing), s2 (transition), s3 (deep squat).
- **Real-Time Feedback:** Visual cues rendered on the video feed based on form.
- **Beginner vs. Pro Thresholds:** Different angle limits based on user expertise.

### 🚨Problem Statements

- **Problem 1:** Users often perform squats with incorrect posture, risking injuries.
- **Problem 2:** Manual form correction is not scalable in home workouts or online fitness training.
- **Problem 3:** Lack of real-time systems that give corrective feedback for body posture during workouts.

### 🔎Loopholes or Research Areas

- **Generalization:** Adapting the model to different lighting, clothing, and body types.
- **Camera Dependency:** Performance can degrade with poor camera placement or quality.
- **Lack of Depth Data:** 2D pose estimation might misinterpret depth or overlap issues.

### 💡Proposed Ideas to Solve Problems

1. **Pose Classification-Based Tracking:** Use joint angles and temporal movement to classify squat states.
2. **Camera Alignment Detection:** Ensure video quality by flagging poor camera placement.
3. **Feedback Overlay:** Visually overlay messages to correct form in real time.

### 🛠️ Proposed Solution: Code-Based Implementation

The repository implements a Streamlit-based video processing app with real-time squat detection and feedback. Key features include:

- **Beginner and Pro Modes:** Custom thresholds for joint angles.
- **Visual Feedback System:** Overlays for cues like "Lower your hips" or "Knee over toe."
- **Statistical Summary:** Total reps, improper reps, and quality metrics.

### 🧩 Key Components

- **`app.py`**: Streamlit front-end for video upload, processing, and displaying metrics.
- **`process_frame.py`**: Core processing logic for pose estimation and feedback.
- **`thresholds.py`**: Defines angle thresholds for beginner and pro modes.
- **`utils.py`**: Drawing functions, angle calculations, and MediaPipe helpers.

## ⚙️ Model Workflow

1. **Input:**

   - **Video Upload:** User uploads a video through the web interface.
   - **MediaPipe Pose Detection:** Extracts joint landmarks from each frame.

2. **Squat Analysis:**

   - **Angle Calculation:** Calculates vertical angles for hip, knee, and ankle joints.
   - **Posture Classification:** Determines the squat state (`s1`, `s2`, `s3`) using thresholds.
   - **Feedback Logic:** Evaluates joint angles and provides visual warnings or positive feedback.

3. **Output:**

   - **Annotated Video Frames:** Each frame is rendered with joint overlays and messages.
   - **Statistical Metrics:** Reps count, incorrect form count, average quality, and more.

## 🚀 How to Run the Code

1. **Clone the Repository:**

    ```bash
    git clone https://github.com/BRAIN-Lab-AI/Pose-Recognition-in-Sports.git
    ```

2. **Set Up the Environment:**

   ```bash
   python3 -m venv venv
   source venv/bin/activate  # On Windows use: venv\Scripts\activate
   pip install -r requirements.txt
   ```

3. **Launch the App:**

   ```bash
   streamlit run app.py
   ```

4. **Upload a Video and Get Feedback:**

   - Choose **Beginner** or **Pro** mode.
   - Upload a workout video.
   - Watch real-time analysis and review workout metrics.
   
   
   ## 🗂️ Project Structure

```
.
├── app.py                     # Main Streamlit interface
├── process_frame.py           # Pose processing logic
├── thresholds.py              # Angle thresholds for analysis
├── utils.py                   # Drawing & helper functions
├── analysis_results/          # Saved JSON reports
├── input videos/              # Sample videos 
└── README.md
```

## 🌟Future Improvements

- [ ] Real-time webcam support
- [ ] Add more exercises (e.g., lunges, push-ups)
- [ ] CSV and Excel report exports
- [ ] Interactive charts (matplotlib / Plotly)
- [ ] Mobile-friendly UI
- [ ] Voice guidance for live feedback



## 🙏 Acknowledgments

- **Open-Source Contributors:**
- [Python](https://www.python.org/)
- [MediaPipe](https://mediapipe.dev/)
- [OpenCV](https://opencv.org/)
- [Streamlit](https://streamlit.io/)
- **Mentors & Reviewers:** Thanks to Dr. Muzammil Behzad for his guidance and for providing us with the opportunity to gain this valuable experience.





---

