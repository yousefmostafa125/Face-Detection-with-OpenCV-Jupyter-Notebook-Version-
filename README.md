# Face Detection with OpenCV (Jupyter Notebook Version)

This notebook demonstrates real-time face detection using OpenCV's **Haar Cascade** classifier and your computer's webcam.

<div style="text-align: center;">
  <img src="Screenshot 2025-08-12 192302.png" alt="My cat" width="300">
</div>

## 📌 Features
- Uses OpenCV's pre-trained `haarcascade_frontalface_default.xml` model.
- Captures a live video feed from your webcam.
- Detects faces in real-time and draws green rectangles around them.
- Press **`q`** to stop the webcam feed.

---

## 🛠 Requirements
You will need:

```bash
python 3.x
opencv-python
jupyter
```

Install the dependencies with:

```bash
pip install opencv-python jupyter
```

---

## ▶ Running the Notebook
1. Open a terminal in the project folder.
2. Start Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
3. Open `code.ipynb` in your browser.
4. Run the cell containing the code.
5. A webcam window will pop up showing real-time video with detected faces.
6. Press **`q`** in the webcam window to stop.

---

## 📂 How It Works
1. **Load Haar Cascade**:  
   ```python
   face_cascade = cv2.CascadeClassifier(cv2.data.haarcascades + 'haarcascade_frontalface_default.xml')
   ```
2. **Capture Video**:  
   `cv2.VideoCapture(0)` starts the webcam.
3. **Detect Faces**:  
   - Convert frame to grayscale for faster processing.  
   - Use `detectMultiScale()` to find face locations.
4. **Draw Rectangles**:  
   Each detected face gets a green bounding box.
5. **Display Video**:  
   `cv2.imshow()` shows the live video feed until `q` is pressed.

---

## ⚠ Notes
- Ensure your webcam is connected and not used by another app.
- Works best in well-lit environments.
- Haar Cascade is fast but may be less accurate than deep-learning-based methods like DNN or MTCNN.
