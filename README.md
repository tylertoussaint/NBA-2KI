# NBA-2KI
A computer vision AI which allows for an immersive experience in the PC game NBA 2k23

### Real-Time Body Gesture Detection and Interaction with PyDirectInput
This Python script combines the power of the MediaPipe Pose model and the `pydirectinput` library to detect and recognize real-time body gestures and movements. It captures video input from the default camera (usually the webcam) and processes the frames to identify specific gestures and actions. Additionally, it uses `pydirectinput` to simulate keyboard events based on the recognized gestures.

***Download nba2kiVid.mp4 to view gameplay

### Why build this?
For years, NBA 2k and Take-Two Interactive have been the leading producer of basketball video games for both console and PC. With virtually no competition, thousands of players come back every September to purchase the newest edition and then continue to spend throughout the year by buying VC (in-game currency). Although great for the company, the influx of money allows for Take-Two to be satisfied with their product and often leads to overlooking consumer complaints. Recently, the addition of crossplay brought to light the neglect faced by PC users and being ranked the second worst game on steam this year, NBA 2k was finally called out on their lack of time spent on their PC platform. PC players deal with an older generation of the game and loss of functions when using a keyboard, and as a result NBA 2k for PC feels like a different game entirely. So why not make it a different game entirely? With the use of this program, PC players now have a unique and immersive experience giving users a new purpose to playing the game and driving more users to join the community.
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

![shooting](https://github.com/tylertoussaint/NBA-2KI/assets/87991331/d2175401-0a0a-43b3-9585-e6f8476fb839)

### Shot Finished
With wrists still above shoulder fully extend one arm past an angle of 165

![shotFinished](https://github.com/tylertoussaint/NBA-2KI/assets/87991331/564e7389-99b0-445c-8e73-341cfdadf0b9)


### Right cross
Right wrist must be below and to the left of the right hip

![rightcross](https://github.com/tylertoussaint/NBA-2KI/assets/87991331/253fab73-e015-49ca-b19a-835e3e93dfdc)

### Left cross
Left wrist must be below and to the right of the left hip

![leftcross](https://github.com/tylertoussaint/NBA-2KI/assets/87991331/1ac977d5-0716-44bd-a457-4b4e3304ef6f)

### Stepback
Turn in either direction facing perpendicular to the camera

![stepback](https://github.com/tylertoussaint/NBA-2KI/assets/87991331/5747d347-486e-42a5-8ff3-dd4c066dd9b9)


## Usage
- Run the script in a Jupyter Notebook or any Python environment (suggest Jupyter Notebook as dependecies and libraries already installed).
  - https://docs.jupyter.org/en/latest/install/notebook-classic.html (download instructions for jupyter notebook)
- Make sure you have a webcam or camera connected for real-time gesture detection.
- Make sure key bindings in 2k are set to:
  - Shooting: 1
  - Pro Stick Left:9
  - Pro Stick Right: 0
  - Pro Stick Down: 8
- Perform the supported gestures in front of the camera to see the corresponding events recognized and displayed. The script will provide feedback and simulate keyboard events using `pydirectinput`.
