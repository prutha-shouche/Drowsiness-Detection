# Drowsiness-Detection

## Description:

Driver fatigue is a significant factor in a large number of road accidents that mainly happen due to human error. The development of technologies for detecting or preventing drowsiness of the drivers at the earliest stage itself is a major challenge in the field of accident avoidance systems. This is a project based on the implementation of Artificial Intelligence and OpenCV concepts to detect drowsiness of a person and sound an alarm once detected.

In the proposed algorithm, first, video data is collected and analyzed using a new approach. In this approach, the image frames taken are enhanced with a sharpening module. Second, a new interpretation of these frames and a combination of the results of the facial key features will be presented for every extracted bounding box. The new interpretation will lead to a clearer and better distinction of the states of features. Finally, we will present a new decision-making algorithm which will result in a more robust drowsiness detection and less false alarms. The rest of the section describes the implementation, flow and working for the system.

## Code Requirements:

The code is compiled in Python (version 2.7 or higher will work, preferably version 3.6) Anaconda Platform is used, from which spyder v3.6 was used. Visual Studio (C++ distribution version also needs to be installed to set up the environment)
The data File has also been included in the repo - face_landmarks.dat_2

## Overview of the Project:

Real time eye tracking in the video is possible with Haar cascades and Camshift Algorithm.
- Haar Cascade: also known as the Viola Jones Face detection technique, is an object detection algorithm used to identify faces in an image or a real time video. It uses edge or line detection.
- Camshift Algorithm (Continuously adaptive mean shift): Applies mean shift algorithm first. Once the mean shift converges, it updates the size window. It also calculates the orientation of the best fitting ellipse to it.
- Mean shift Algorithm: Assigns data points to the cluster iteratively by shiftomg points towards the node (highest density of the datapoints in the region)

Following features are extracted from the face and based on the input from each frame, the algorithm provides the output.
- Eye Aspect Ratio
- Mouth Aspect Ratio
- Blink Count
- Yawn Count
- Crucial Facial Points
- Convex Hull

## Dependencies:

Libraries such as: 

-cv2
-dlib
-cmake
-scikit learn
-imutils
-scipy

should be installed and imported.

## Procedure:

-A model is built for drowsiness detection of a driver by real-time Eye-Tracking in videos using Haar Cascades and CamShift algorithm.

-Used the significant features for each video frame extracted by the algorithm to stitch as a sequence of feature vectors for consecutive frames.

-Detect Face and Eyes in a Single Image: The face is detected using a shape detector which is a pre-installed file: face_landmarks.dat_2

## Execution:

-To run the code, type python Drowsiness_Detection.py in the command prompt or F5 when using spyder.

The final output has the following information for the series of frames taken as input.

-Eye Aspect Ratio: The Eye Aspect Ratio is a constant value when the eye is open, but rapidly falls to 0 when the eye is closed. It is an estimate of the eye-opening state.

-Mouth Aspect Ratio: The Mouth Aspect Ratio is a constant value when the mouth is open, but rapidly falls to 0 when the mouth is closed. It is an estimate of the mouth-opening state.

-Blink count: Counts the total number of times the eye blinks every second, typically involving a combination of: -Eye localization. -Thresholding to find the whites of the eyes. -Determining if the “white” region of the eyes disappears for a period of time (indicating a blink).

-Yawn Count: Counts the total number of times the yawning takes place every second

-Shows the crucial facial points: We can apply facial landmark detection to localize important regions of the face, including eyes, eyebrows, nose, ears, and mouth. Facial landmarks can be used to align facial images to mean face shape so that after alignment the location of facial landmarks in all images is approximately the same.

-Convex Hull Face: Detects the boundry of the face. (A convex object is one where no interior angle is greater than 180 degrees, Hull - exterior shape of the object) 
