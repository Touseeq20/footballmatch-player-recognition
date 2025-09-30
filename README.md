# ⚽ Football Player & Ball Detection using OpenCV

This project detects **football players (Team A in Blue, Team B in Red)** and the **football (white)** from a match video using **OpenCV** and **color-based segmentation** in HSV color space.  

It draws bounding boxes and labels players/ball frame by frame.

---

## 📂 Project Structure
```
├── cutvideo.mp4        # Input football match video
├── PlayerRecognition.py        # Detection script (this file)
└── Cropped/            # Extracted frames
```

---

## 🔧 Requirements

Install the dependencies before running the script:

```bash
pip install opencv-python numpy
```

---

## ▶️ Usage

1. Place your video in the project folder and rename it to **cutvideo.mp4** (or update path in code).
2. Run the script:
   ```bash
   python detection.py
   ```
3. Press **Q** to quit the live display.

---

## 🎯 Features
- Detects **Team A (Blue jerseys)** players.
- Detects **Team B (Red jerseys)** players.
- Detects **Football (white ball)**.
- Saves processed frames inside the **Cropped/** folder.
- Displays live annotated video with bounding boxes.

---

## ⚙️ How It Works
1. Reads video frame by frame using **OpenCV**.
2. Converts frame into **HSV color space**.
3. Applies color ranges:
   - Green → Field masking  
   - Blue → Team A  
   - Red → Team B  
   - White → Ball  
4. Detects contours → filters by size (to separate players vs ball).
5. Draws bounding boxes with labels:
   - 🟦 Blue box → Team A player  
   - 🟥 Red box → Team B player  
   - 🟩 Green box → Football  

---

## 🚀 Future Improvements
- Replace color segmentation with **YOLO/DeepSORT** for better accuracy.
- Add **jersey number recognition** using OCR.
- Track ball trajectory & detect **goals/fouls**.

---

## 👨‍💻 Author
Muhammad Touseeq  

