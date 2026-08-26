**Office Posture Monitor MediaPipe**

A real-time computer vision project that monitors office posture using a webcam and saves the processed output video automatically.
Features
Real-time webcam-based posture monitoring
MediaPipe-based pose analysis
Calibration support for establishing a reference posture
Posture status detection
Posture score calculation
Shoulder and neck alignment analysis
Live visual feedback on the processed frame
Video recording of the processed output
GitHub link displayed in the bottom-right corner of the recorded video
Automatic saving of the output video in the current working folder
Technologies Used
Python
OpenCV
MediaPipe
NumPy
Project Files
```text
Office_Posture_Monitor/
│
├── Office_Posture_Monitor_With_Recording.ipynb
├── posture_output.mp4
└── README.md
```
> `posture_output.mp4` is created after running the recording cell.
Installation
Install the required libraries:
```bash
pip install opencv-python mediapipe numpy
```
**How to Run
Step 1:** Open the notebook
Open:
```text
Office_Posture_Monitor_With_Recording.ipynb
```
**Step 2:** Run all setup and class-definition cells
Execute the notebook cells in order so that the `OfficePostureMonitor` class and required functions are available.
**Step 3:** Run the recording cell
The webcam will open and the posture monitoring system will begin processing frames.
The processed frame is:
Displayed live
Recorded to a video file
Stamped with the GitHub link in the bottom-right corner
The recording uses:
```python
github_link = "github.com/ajanthadevi2012"
output_path = "posture_output.mp4"
```
**Step 4:** Stop recording
Press:
```text
Q
```
The camera and video writer will then be released automatically.
Output
After recording is stopped, the generated video is saved in the current working directory:
```text
posture_output.mp4
```
The notebook also prints the absolute path of the saved output.
Recording Flow
```text
Webcam
   │
   ▼
Capture Frame
   │
   ▼
OfficePostureMonitor
   │
   ├── Pose / Posture Analysis
   ├── Calibration Reference
   ├── Shoulder Analysis
   ├── Neck Analysis
   ├── Posture Status
   └── Posture Score
   │
   ▼
Processed Video Frame
   │
   ├── Display Live
   ├── Add GitHub Link
   └── Save Using VideoWriter
          │
          ▼
   posture_output.mp4
```
GitHub Watermark
The GitHub reference is added to the bottom-right corner of every processed frame before it is written to the output video:
```text
github.com/ajanthadevi2012
```
To use another repository or profile, change:
```python
github_link = "github.com/ajanthadevi2012"
```
**Suggested Dashboard Extensions**
The current project can be extended with the following dashboard features:
Session timer
Good vs poor posture duration
Warning counter
Posture history
CSV session logging
Automatic screenshot capture for prolonged poor posture
Posture trend graph
Daily/session summary
Break reminders
These can be added as a dashboard overlay or as a separate Streamlit/Flask web dashboard.
Requirements
```text
Python 3.9+
opencv-python
mediapipe
numpy
```
Notes
Ensure that webcam permissions are enabled.
If the default camera does not open, change:
```python
cap = cv2.VideoCapture(0)
```
to another camera index such as:
```python
cap = cv2.VideoCapture(1)
```
The output video is saved relative to the folder from which the notebook is running.
**Author
GitHub: github.com/ajanthadevi2012
**
