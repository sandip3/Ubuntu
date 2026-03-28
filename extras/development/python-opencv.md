# 🐍 Python & OpenCV Setup

---

## 🔙 Back to Extras

👉 [Go to Extras Index](../index.md)

---

### 🏷️ Command Compatibility

* 🟢 LTS → Stable for Ubuntu LTS (22.04, 24.04)
* 🔵 Non-LTS → For newer Ubuntu releases (23.x, 25.x)
* ⚪ Universal → Works on all versions

---

## 19. Update System 🔄

⚪ Universal

```bash id="a1d9k3"
sudo apt update
sudo apt upgrade -y
```

---

## 20. Install Dependencies 📦

⚪ Universal

```bash id="m2f8x7"
sudo apt install python3-dev python3-pip python3-numpy build-essential \
libgtk-3-dev libavcodec-dev libavformat-dev libswscale-dev libv4l-dev \
libxvidcore-dev libx264-dev libjpeg-dev libpng-dev libtiff-dev \
gfortran openexr libatlas-base-dev -y
```

---

## 21. Install OpenCV 🧠

⚪ Universal

```bash id="p3g6r2"
pip3 install opencv-python
```

---

## 22. Verify Installation ✅

⚪ Universal

```bash id="v8q4z1"
python3
```

Then inside Python:

```python id="c5n2y9"
import cv2
print(cv2.__version__)
```

---

## 23. Optional: Extra OpenCV Modules

⚪ Universal

```bash id="j7x3m6"
pip3 install opencv-contrib-python
```

---

## 💡 Recommended: Virtual Environment

⚪ Universal

```bash id="k4t9p1"
python3 -m venv venv
source venv/bin/activate
pip install opencv-python
```

---

## 💡 Notes

* Always prefer **virtual environments** for Python projects
* OpenCV installation may take time depending on dependencies
* Use `opencv-contrib-python` for advanced features

---

> ⬅️ Previous: [GitHub Setup](./github-setup.md) | ➡️ Next: [Anki Extensions](../learning/anki-extensions.md)
