# 🚗 Vehicle Counting System using YOLOv8 & SORT

![Demo](data/Cars.gif)

## 📌 Overview
This project implements a **Vehicle Counting System** using **YOLOv8** for object detection and **SORT** for object tracking.  
The system detects and tracks vehicles (cars, trucks, buses, motorbikes) from video streams, applies region masking, and counts the number of vehicles crossing a predefined line.

## ✨ Features
- Vehicle detection using YOLOv8 (cars, buses, trucks, motorbikes).
- Object tracking with SORT algorithm.
- Region masking for focused detection.
- Real-time vehicle counting across a virtual line.
- Customizable counting line and mask regions.

## 📂 Project Structure
Vehicle-Counting-YOLOv8/
│── data/
│   ├── cars.gif       # Sample gif for testing
│   ├── mask.png        # Region mask for focused detection
│   └── graphics.png    # Overlay graphics
│
│── src/
│   ├── car_counter.py  # Main script
│   └── sort.py         # SORT tracking algorithm
│
│── weights/
│   └── yolov8n.pt      # YOLOv8 model weights (download separately if large)
│
│── requirements.txt    # Dependencies
│── README.md           # Project documentation
│── .gitignore

## ⚙️ Installation
git clone https://github.com/omarahatem44/Vehicle-Counting-YOLOv8.git
cd Vehicle-Counting-YOLOv8

# Create a virtual environment (recommended)
python -m venv venv
source venv/bin/activate   # For Linux/Mac
venv\Scripts\activate      # For Windows

# Install dependencies
pip install -r requirements.txt

## ▶️ Usage
# Place your input video in the `data/` folder.
python src/car_counter.py

# Press `q` or `ESC` to exit.

## 📊 Results
The system will:
- Detect vehicles in the video.
- Track them using unique IDs.
- Count vehicles when crossing the defined line.  

Example Output:
Count: 37 vehicles

## 📌 Future Improvements
- Add support for more object classes (e.g., bicycles, pedestrians).
- Optimize for real-time video streams (CCTV/webcam).
- Deploy as a web or mobile application.

## 🤝 Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## 📜 License
This project is licensed under the MIT License - see the LICENSE file for details.
