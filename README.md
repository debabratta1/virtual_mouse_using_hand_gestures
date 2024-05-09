1.1 Introduction About Project:-
The world is full of technology driven factors in our day to day life. We have so many 
technologies, throughout the world computer technologies are growing simultaneously. They 
are used to perform various tasks which cannot be performed by humans. In fact they are ruling 
the human lives because they have a potential to do the tasks which cannot be done by humans. 
The interaction between human and computer can be done with output device like mouse. The 
mouse is a device used for interacting with a GUI which includes pointing, scrolling and 
moving etc. 

 

Data flow diagram: -
![Screenshot 2024-05-09 205935](https://github.com/debabratta1/virtual_mouse_using_hand_gestures/assets/157493392/2a023c6e-19a7-4daf-bd12-09b849d8b1ab)

 Explanation:-
1. Hand Image: The process starts with a digital image captured by a camera. This image 
is assumed to contain a hand.
2. Hand Detection: In this stage, the system isolates the hand from the background and 
other objects in the image. There are various hand detection algorithms that can be used 
for this purpose, such as skin color segmentation or background subtraction.
 

3. Preprocessing: Once the hand is detected, the image is preprocessed to improve the 
quality of the data for the next stage. Preprocessing techniques can include noise 
reduction, contrast enhancement, and image normalization.
4. Feature Extraction: In this stage, the system extracts a set of features from the 
preprocessed image that represents the characteristics of the hand gesture. These 
features can include the geometric properties of the hand, such as the fingertip locations, 
angles between fingers, or the palm orientation.
5. Recognition (Gesture Dictionary): The extracted features are then matched against a 
database of stored gestures, also known as a gesture dictionary. This dictionary contains 
a collection of reference templates representing previously learned hand gestures. A 
recognition algorithm compares the features of the unknown gesture with the templates 
in the dictionary to find the best match.
6. Execution (Command): Based on the recognized gesture, a corresponding action or 
command is executed by the system. For instance, if the recognized gesture is a swipe 
to the right, the system might interpret this as a command to turn to the next page of a 
book.


 Overview of Project:-
 
The development of a hand gesture recognition algorithm for fourteen hand gestures 
based on finger counting represents a significant advancement in human-computer 
interaction. By leveraging the maximum distance between the centroid of the fingers, 
the algorithm accurately identifies and distinguishes between various gestures.
The application of this algorithm in the creation of an AI virtual mouse using hand 
gestures presents an innovative and exciting technology with transformative potential. 
By harnessing the power of a real-time camera, the system enables users to seamlessly
manage the mouse pointer and perform its functions without the need for a traditional 
input device.
This approach offers users a more natural, intuitive, and accessible method of 
controlling the cursor on the screen, enhancing overall user experience. Moreover, the 
integration of voice assistant support further elevates the functionality of the virtual 
mouse system.
With voice assistant integration, users gain additional control over their devices by 
issuing voice commands to execute a wide range of tasks, including opening 
applications, navigating menus, performing web searches, and controlling the cursor 
using hand gestures.
As technology continues to advance, we anticipate the emergence of even more 
innovative solutions that enhance user experience and improve accessibility for all 
individuals, further bridging the gap between humans and computers. The synergy 
between hand gesture recognition and voice assistant technology represents a promising 
frontier in human-computer interaction, paving the way for more intuitive and seamless 
 
 Key Features:
Key features of a virtual mouse project include cursor movement simulation, left and 
right-click actions, and scrolling functionality. It should support various input 
methods such as touchscreens, keyboards, and specialized devices for accessibility. 
Compatibility across multiple platforms and operating systems is crucial for 
widespread adoption. Customizable settings for sensitivity, acceleration, and button 
mapping enhance user experience. Accessibility features like keyboard shortcuts and 
high-contrast modes cater to diverse user needs. Integration with existing software 
applications and frameworks should be seamless. Performance optimization to 
minimize latency and ensure responsiveness is essential. Thorough testing across 
different use cases and user groups ensures reliability. Comprehensive 
documentation and user support resources aid in usability and troubleshooting. 
Continuous updates and future scalability ensure the longevity and relevance of the 
virtual mouse solution

Libraries used in project:-
OpenCV (cv2): OpenCV (Open Source Computer Vision Library) is a popular library for
computer vision and image processing tasks.
In this code, OpenCV is used for capturing video from the webcam, processing frames, and detecting
hand landmarks.
Mediapipe (mp):Mediapipe is a framework for building multimodal (e.g., video, audio) applied
machine learning pipelines.
In this code, Mediapipe's hand tracking solution is utilized to detect and track hand landmarks in real
time.
PyAutoGUI: PyAutoGUI is a Python module for programmatically controlling the mouse and
keyboard. It is used in this code to simulate mouse movements and clicks based on the detected hand
gestures.
math: The math module provides mathematical functions and constants in Python.
It is used in this code for mathematical calculations, such as computing distances between hand
landmarks.
Enum (IntEnum): The Enum module in Python provides a way to create enumerated constants.
In this code, IntEnum is used to define enumerations for hand gestures and label types.
ctypes: The ctypes module provides a way to access C data types and functions from Python.
It is used in this code for accessing functionality from the Windows Core Audio API through COM
interfaces.
comtypes: The comtypes library provides Python bindings for the Component Object Model (COM).
It is used in conjunction with ctypes for accessing and controlling audio endpoints in the Windows 
Core Audio API.
 
pycaw: The pycaw library is a Python wrapper for the Windows Core Audio API.
It is used in this code for interacting with audio devices, specifically for controlling the system
volume.
google.protobuf.json_format: The google.protobuf.json_format module provides functions for
converting Protocol Buffer messages to and from JSON format.
It is used in this code for converting Mediapipe hand tracking results to a dictionary format for easier
manipulation.
 
2.1 Software and Hardware specifications:
➢ Jupyter notebook ide6.4.0
➢ Visual Studio Code (Editor & Application Development Environment)
➢ google colab
2.2 Languages support Software:
➢ Python Script
2.3 Hardware requirements:
➢ Operating system: windows 11
➢ Processor: Intel® CoreTM i5-7020 CPU @ 2.30GHz
➢ System type: 64-bit Operating System
➢ RAM: 8 Gb or more
➢ Hard drive: 128GB or more
2.4 Technologies Used:
➢ PyAutoGui
➢ OPENCV
➢ MEDIAPIPE
CHAPTER – 2
HARDWARE / SOFTWARE REQUIREMENTS 
AND TECHNOLOGY 
 

For the purpose of hand and finger detection we are using the one of the effective open source 
library mediapipe, it is one type of the framework based on the cross platform features which 
was developed by google and Opencv to perform some CV related tasks. This algorithm uses 
machine learning related concepts for detecting the hand gesture and to track their movements
3.1 Media pipe:
Google created the open-source MediaPipe framework to enable the development of cross-platform, 
real-time computer vision applications. For processing and analyzing video and audio streams, it 
offers a number of pre-made tools and components, such as object detection, pose estimation, hand 
tracking, facial recognition, and more.
Developers can quickly construct intricate pipelines using MediaPipe that combine numerous 
algorithms and processes and execute in real-time on a variety of h/w platforms, like CPUs, GPUs, 
and specialized accelerators like Google's Edge TPU. Additionally, the framework has interfaces 
helps us interacting with other well-liked machine learning libraries, including TensorFlow and 
PyTorch, and it supports several programming languages, like C++, Python, and Java.
For computer vision and ML tasks, MediaPipe is a comprehensive library that offers a many of 
features. Here are a few of the library's main attributes and features:
1. Video and Audio Processing: MediaPipe provides tools for processing and analyzing video and 
audio
streams in real-time. This includes functionalities such as video decoding, filtering, segmentation, 
and
synchronization.
2. Facial Recognition: MediaPipe can detect and track facial landmarks, including eyes, nose, mouth, 
and eyebrows, in real-time. This functionality is useful for applications such as facial recognition, 
emotion detection, and augmented reality.
3. Hand Tracking: MediaPipe can track hand movements in real-time, allowing for hand gesture 
recognition and interaction with virtual objects.
4. Object Detection: MediaPipe can detect and track objects in real-time using machine learning 
models. This functionality is useful for applications such as augmented reality, robotics, and 
surveillance.
5. Pose Estimation: MediaPipe can estimate the poses of human bodies in real-time, allowing for 
applications such as fitness tracking, sports analysis, and augmented reality.


   
ALGORITHMS AND TOOLS USED
 

For a variety of tasks, such as object detection, position estimation, facial recognition, and more, 
MediaPipe offers tools for training and deploying machine learning models. All in all, MediaPipe 
is a potent tool kit that gives programmers the ability to easily create sophisticated real-time 
computer vision and ML applications.
3.2. ALGORITHM DEVELOPMENT
The proposed algorithm consists of four main parts – image acquisition, pre-processing, 
finger detection, gesture recognition. Figure 1 shows the overall steps involved in a 
successful hand gesture recognition algorithm.
3.2.1. Pre-Processing
After a successful binary image is determined, the image should be cleaned to process 
further. First, the small objects in the image must be removed. Thus, objects which are less 
than a certain pixel must be removed to obtain the object that the user needed. If the object 
has any holes, it should be fixed. This will ensure a good hand gesture recognition. Finally, 
the object inside the image is counted. If the number of the object is one (make sure that 
only the hand is detected in the image), then the algorithm can proceed further.
3.2.2 Finger Detection
First, the centroid of the binary image is determined. This will be the center of the hand 
which will be used to remove the wrist of the hand and palm. After finding the centroid of 
 

the image, the right side of the image which is the wrist will be removed as it does not 
involve the finger detection. Then, the largest distance between one pixel to another on the 
contour of the object is determined using the equidistance formula. The formula of 
equidistance is:
The maximum distance will be divided by two to obtain the radius of the circle. A circle will 
be drawn in the image, and it will be removed (palm) as we obtain the radius and center of 
the circle. Moreover, the radius should times by 1.26 to make the circle bigger so that only 
the fingers can be obtained. The number of an object inside the image will be calculated and
displayed.
3.2.3. 
The detected fingers are classified into their respective finger count. The gestures are 
classified using the maximum distance between the centroid of the two fingers determined 
in the finger detection process. The distance between each centroid of the two fingers is 
determined using the equidistance Equation (3).
3.2.4 Rectangular Region for Moving through the Window
The windows display is marked with the rectangular region for capturing the hand gesture 
to perform mouse action based on the gesture. when the hands are find under those 
rectangular area the detection begins to detect the action based on that the mouse cursor 
functions will be performed. The rectangular region is drawn for the purpose of capturing 
the hand gestures through the web camera which are used for mouse cursor operations. 
Mouse Functions Depending on the Hand Gestures and Hand Tip Detection Using Computer 
Vision:
• For the Mouse Cursor Moving around the Computer Window:
![Screenshot 2024-05-09 210322](https://github.com/debabratta1/virtual_mouse_using_hand_gestures/assets/157493392/76dbb0af-f81c-4fbd-9720-84bd804afc56)

 
i. Pause the cursor (No movement):



 ![pause](https://github.com/debabratta1/virtual_mouse_using_hand_gestures/assets/157493392/ee5233ca-c4b9-4455-b704-138cbbec3d1e)

 
ii. Moving cursor:


 ![movement](https://github.com/debabratta1/virtual_mouse_using_hand_gestures/assets/157493392/c14fa4c8-fcf8-4a31-8829-e82b8ae66d04)

iii. Left click:


![left-click](https://github.com/debabratta1/virtual_mouse_using_hand_gestures/assets/157493392/cb8c8e44-4cf7-40c0-998c-31b1f8e96701)

iv. Right click:


![right-click](https://github.com/debabratta1/virtual_mouse_using_hand_gestures/assets/157493392/d54eb6a9-ff77-4f9d-b076-c293ec5b22ca)



v. Select, Drag and drop:


![select   drag](https://github.com/debabratta1/virtual_mouse_using_hand_gestures/assets/157493392/f6a9a293-dbf1-4e0e-8fe4-6a2b533f0b7a)


vi. To zoom in move horizontally right size and to zoom out move horizontally left 
size


![screen scroll](https://github.com/debabratta1/virtual_mouse_using_hand_gestures/assets/157493392/6179ded8-5d9a-47ef-b856-56882d6c1deb)


vii. To increase brightness move horizontally right size and to decrease brightness 
move horizontally left size:

 
![volume brightness](https://github.com/debabratta1/virtual_mouse_using_hand_gestures/assets/157493392/cf837d62-cdf9-4788-9360-fcdb9ebbdab3)

viii. To scroll down screen move vertically down and to scroll up screen move 
vertically up:


![screen scroll](https://github.com/debabratta1/virtual_mouse_using_hand_gestures/assets/157493392/4d6b024a-5fee-4a7d-9638-a1168c6611b5)

ix. To increase volume move vertically up and to decrease volume move vertically 
down:


![volume brightness](https://github.com/debabratta1/virtual_mouse_using_hand_gestures/assets/157493392/722dbe26-4a70-4a98-9e6d-c94bea17f048)
