# VRCFT-Mic-Toggle
Unity prefab that adds the ability to Toggle On/Off Face Tracking when muting within VRChat when using VRCFT, supports AdJerry's and Pawlygon's FT Prefabs

# PREREQUISITES
[VRCFury](https://vrcfury.com/download/)

Either [AdJerry's](https://github.com/Adjerry91/VRCFaceTracking-Templates) or [Pawlygon's](https://github.com/PawlygonStudio/VRC-Facetracking) VRCFT prefabs

# HOW TO USE
Drag the .unitypackage into your VRC Unity project. Depending on what you have, place either the AdJerry or Pawlygon Mic Toggle Prefab **BELOW** the VRCFT prefab

<img width="500" height="118" alt="Mic toggle" src="https://github.com/user-attachments/assets/45a7d804-c418-412e-a57c-c141fd65b25b" />

# What does it do?
It adds an extra toggle to your VRCFT Menu, when enabled, face tracking will automatically enable when unmuting, and automatically disable when muting

<img width="409" height="343" alt="image" src="https://github.com/user-attachments/assets/aa2ca01a-01e5-46a0-b4d4-3974045b8c25" />

# How does it work?
Uses the "MuteSelf" Animator parameter to detect Mic status and dinamically disables or enables Face and Eye tracking depending on its state, this is a toggleable feature in case you don't want it enabled all the time, but consider it a "nice to have" depending on the situation

# Additional features (ADVANCED)
By default there will be 2 disconnected states, these being *Disable Mouth* and *Disable Eyes*, these are meant to temporarely disable either the mouth or the eyes when performing a hand gesture, example below

<img width="1170" height="502" alt="image" src="https://github.com/user-attachments/assets/4b4b53ef-a9c4-49db-98ff-52c1c0426320" />
If you don't know what you'll use this for, chances are you don't need it

To properly set up this feature, connect the *Tracking Enabled* state and the *Disable Mouth* or *Disable Eyes* to each other depending on what you need
Set the transition to "Disable Eyes" or "Disable Mouth" to **No exit time**, Gesture Left/Right Equals #, # being your hand gesture
Set the transition to "Traching Enabled" with **No exit time**, Gesture Left/Right **NOT EQUALS** #, " being the gesture from above 

<img width="1693" height="536" alt="image" src="https://github.com/user-attachments/assets/cd5311b6-1c61-4148-a75b-14edbfc23864" />

If multiple gestures will disable the eyes or mouth, add a transition to the disable state for each one, you only need one single transition to the **Tracking enabled** state, which will have added conditions instead of transitions, like the img below

<img width="1691" height="533" alt="image" src="https://github.com/user-attachments/assets/699ef9be-0740-4588-89a8-5cbec3bd05ca" />

## This feature is highly experimental and intended for tinckering with automization, requieres high level of unity knowledge and works as a half made template for you to start working with. No support is planned for this feature
