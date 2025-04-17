# 🚘 Car Parking Slot Detection System

This project uses OpenCV to detect available parking slots from a top-down camera view in real-time. It allows manual marking of parking spots and monitors their occupancy using adaptive thresholding and pixel analysis.

---

## 📌 Features

- 🔍 Detects free and occupied parking spaces from video footage
- 🖱️ Interactive parking slot setup using mouse clicks
- 📊 Real-time display of slot status and occupancy counts
- 💾 Saves selected parking slot positions using Pickle
- ♻️ Automatically loops video playback

---

## 🧠 How It Works

1. **Mark Parking Slots**  
   Use the `parking_slot_picker.py` script to mark or delete parking slots on a reference image:
   - **Left click** to add a slot
   - **Right click** to remove a slot

2. **Slot Detection**  
   The `main_detector.py` script:
   - Loads the saved slot positions
   - Detects cars using adaptive thresholding
   - Counts non-zero pixels in each slot to determine occupancy
   - Displays total free and occupied slots on screen

---

## 🛠 Technologies Used

- Python 3
- OpenCV
- NumPy
- Pickle
- cvzone (for enhanced annotations)

---

# Install Required Packages
- pip install opencv-python numpy cvzone

# 📁 File Structure

car-parking-slot-detection/
- carPark.mp4               # Input video of parking lot
- carParkImg.png            # Reference image for marking slots
- CarParkPos                # Pickle file to store parking slot positions
- main_detector.py          # Main script to run detection
- parking_slot_picker.py    # Tool to define parking slot 


# 📽️ Usage

-Step 1: Select Parking Slots
   - python parking_slot_picker.py
   - A window will appear with carParkImg.png
   - Use left-click to mark new slots, right-click to remove.
   - Slot positions will be saved to CarParkPos.
-Step 2: Run the Detector
   - python main_detector.py
   - Processes carPark.mp4.
   - Displays slots with colored rectangles:
        -🟩 Green = Free
        -🟥 Red = Occupied
   - Shows live counter of available slots.

📷 Screenshots

<img width="832" alt="image" src="https://github.com/user-attachments/assets/d87b0b4c-c42b-47ff-b572-354be91156aa" />


# 🙋‍♂️ Author

Hema Kiran Reddy
B.Tech CSE (AIML) | Christ University, Bangalore
GitHub: yourusername

# 📄 License

This project is open-source and free to use for academic or research purposes.






