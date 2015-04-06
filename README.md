# The eleVR webVR Boilerplate
This is the standard ThreeJS-based boilerplate for webVR currently being used by [the eleVR team](http://elevr.com). It is a starting point for web-based VR experiences that work with the Oculus Rift as well as with smartphones + a google cardboard or similar phoneVR headset. There is also a non-VR fallback for experiencing the content without a VR device.

The boilerplate also has gamepad and keyboard controls that are on by default. 

# Controls:
Click (or tap) to enter full-screen VR mode.

Navigation Controls:
- WASD + E/Q navigation support for rotation.
- Arrow key navigation support for moving the location of the camera.
- Gamepad joystick navigation controls.
- Orientation control with a VR headset OR mobile phone.

# Explanation of Files:
index.html
- A simple html file with a very basic example THREE.js experience built in. 
- When using this as a boilerplate, you would generally only modify this file.

[THREE.js (three.min.js)](https://github.com/mrdoob/three.js/)
- WebGL helper library that lets you create webGL experiences using JS.
PhoneVR.js (special thanks to [Andrew Lutomirski](https://github.com/amluto) for helping with this)
- Detects whether a device with orientation is being used and turns phone orientation data into a quaternion.

VRControls.js [(forked from MozVR version)](https://github.com/MozVR/vr-web-examples/tree/master/threejs-vr-boilerplate)
- THREE.js controls which take advantage of the WebVR API.
- Keyboard controls
- Gamepad controls
- Pulls in phoneVR information for phoneVR controls

VREffect.js [(forked from MozVR version)](https://github.com/MozVR/vr-web-examples/tree/master/threejs-vr-boilerplate)
- THREE.js effect which renders a scene with two cameras in it side by side when in webVR or on a phone for VR viewing, but just a single camera full-screen as a fallback for non-VR viewing.

# Acknowledgements
This boilerplate is based on [Mozilla's boilerplate](https://github.com/MozVR/vr-web-examples/tree/master/threejs-vr-boilerplate)

It has been developed with the advice, help, and contributions of a great many people including (but not limited to) the other members of the eleVR team (Emily Eifler and Vi Hart), [Andrew Lutomirski](https://github.com/amluto), and Henry Segerman.

