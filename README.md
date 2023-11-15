# NBA-2KI
A computer vision AI which allows for an immersive experience in the PC game NBA 2k23

### Real-Time Body Gesture Detection and Interaction with PyDirectInput
This Python script combines the power of the MediaPipe Pose model and the `pydirectinput` library to detect and recognize real-time body gestures and movements. It captures video input from the default camera (usually the webcam) and processes the frames to identify specific gestures and actions. Additionally, it uses `pydirectinput` to simulate keyboard events based on the recognized gestures.

***Download `nba2kiVid.mp4` to view gameplay (slight lag in program due to OBS recording)

### Why build this?
For years, NBA 2k and Take-Two Interactive have been the leading producer of basketball video games for both console and PC. With virtually no competition, thousands of players come back every September to purchase the newest edition and then continue to spend throughout the year by buying VC (in-game currency). Although great for the company, the influx of money allows for Take-Two to be satisfied with their product and often leads to overlooking consumer complaints. Recently, the addition of crossplay brought to light the neglect faced by PC users and being ranked the second worst game on Steam this year, NBA 2k was finally called out on their lack of time spent on their PC platform. PC players deal with an older generation of the game and loss of functions when using a keyboard, and as a result NBA 2k for PC feels like a different game entirely. So why not make it a different game entirely? With the use of this program, PC players now have a unique and immersive experience giving users a new purpose to playing the game and driving more users to join the community.
## Key Features

### Shooting Gesture Detection
The code can identify when a "shooting" gesture is performed. It checks if both wrists are positioned above the shoulders and if the angles of the left and right elbows are less than 165 degrees. When this gesture is detected, it registers a "Shooting" event and simulates a keyboard keypress using `pydirectinput`.

### Shot Finished Gesture Detection
Similarly, it recognizes when a "shot finished" gesture occurs. If both wrists are above the shoulders and the angles of the left or right elbows are greater than 165 degrees, it registers a "Shot Finished" event and releases the keyboard key using `pydirectinput`.

### Crossing Gestures
The code also detects "right cross" and "left cross" gestures. These are recognized when the wrists are positioned below and to the right or left of the respective hips. 

### Step Back Gesture
The "stepback" gesture is identified when the distance between the shoulders and hips is relatively small. This suggests a step back motion when standing sideways.

### User Feedback
The code provides real-time feedback on the recognized gestures by displaying the detected events on the screen. It also uses `pydirectinput` to simulate keyboard events when certain gestures are detected.

### Visualizations
The script draws landmarks and skeletal connections on the video frames to help visualize the body's pose and movements. It also displays the most recent detected events at the top of the video frame.

### Controller functionality
By using a controller the user can also perform the actions in game not currently covered by the program (i.e. moving around)

## Gesture Guide

### Shooting
Raise both wrists above the shoulders

![shooting](https://github.com/tylertoussaint/NBA-2KI/assets/87991331/dfe1daf6-cf3d-449c-9e6c-3c3c2ba24421)

### Shot Finished
With wrists still above shoulder fully extend one arm past an angle of 165

![shotFinished](https://github.com/tylertoussaint/NBA-2KI/assets/87991331/20ff35a0-7ae0-4743-853b-01668c60bae6)

### Right cross
Right wrist must be below and to the left of the right hip

![rightcross](https://github.com/tylertoussaint/NBA-2KI/assets/87991331/ad07c434-3fc4-4d32-b3b1-34ef272ae644)

### Left cross
Left wrist must be below and to the right of the left hip

![leftcross](https://github.com/tylertoussaint/NBA-2KI/assets/87991331/196ac0ea-75e4-4acb-9163-72ae924716f6)

### Stepback
Turn in either direction facing perpendicular to the camera

![stepback](https://github.com/tylertoussaint/NBA-2KI/assets/87991331/16c41df0-e685-4270-a7dd-b8db284e2ab2)

## Usage
- Run the script in a Jupyter Notebook or any Python environment (suggest Jupyter Notebook as dependencies and libraries already installed).
  - https://docs.jupyter.org/en/latest/install/notebook-classic.html (download instructions for jupyter notebook)
- Make sure you have a webcam or camera connected for real-time gesture detection.
- Make sure key bindings in 2k are set to:
  - Shooting: 1
  - Pro Stick Left:9
  - Pro Stick Right: 0
  - Pro Stick Down: 8
- Perform the supported gestures in front of the camera to see the corresponding events recognized and displayed. The script will provide feedback and simulate keyboard events using `pydirectinput`.
