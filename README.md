# Motion-detection-Alarm-System
The Motion Detection Alarm System is a Python-based real-time surveillance tool that uses computer vision to detect movement through a webcam and triggers an audible alarm if motion is detected. 

Live Camera Feed: Utilizes OpenCV to capture video frames from the default camera.

Motion Detection Logic: Converts video frames to grayscale and applies Gaussian blur to reduce noise. Compares each new frame to a reference (starting) frame using cv2.absdiff and thresholding. If the motion surpasses a sensitivity threshold, it counts as movement.

Alarm System: Once significant movement is detected repeatedly (more than 20 times), an alarm is triggered using winsound.Beep. The alarm runs in a separate thread to avoid blocking the video feed.

User Controls: Press T to toggle motion detection (alarm mode). Press Q to quit the program safely.
