# The eleVR webVR Boilerplate
This is the standard ThreeJS-based boilerplate for webVR currently being used by [the eleVR team](http://elevr.com). It is a starting point for web-based VR experiences that work with the Oculus Rift as well as with smartphones + a google cardboard or similar phoneVR headset. There is also a non-VR fallback for experiencing the content without a VR device.

The boilerplate also has gamepad and keyboard controls that are on by default. 

If you would like to use this boilerplate as a starting point for your own VR projects, check out brief tutorial for doing so at the bottom of this page.

# Controls:
Click (or tap) to enter full-screen VR mode.

Navigation Controls:
- WASD + E/Q navigation support for rotation.
- Arrow key navigation support for moving the location of the camera.
- Gamepad joystick navigation controls.
- Orientation control with a VR headset OR mobile phone.

# Explanation of Files:
index.html
- A simple html file. 
- By default, it points at demoWebVR.js, which contains a demo webVR experience
- You can change it to point at blankWebVR.js, which is clearly annotated for creating your own experience

demoWebVR.js
- A basic demo THREE.js experience is written into this file, you can use it as a guideline.

blankWebVR.js
- A clearly annotated boilerplate file that you can add code to to create your own webVR project from scratch

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

# WebVR Basic Tutorial
1. Obtain a webVR browser (we recommend Firefox Nightly) for your OS
1a. Also get the appropriate Oculus runtime if you are going to use with an Oculus
2. If you are using Firefox Nightly, enable webVR in your browser
  - enter "about:config" into your address bar
  - use the search tool to find "vr"
  - then set "dom.vr.enabled" to "true"
3. Edit demoWebVR.js in the webVR-boilerplate/js folder to create your scene.
  - It has some sample code already to get you started
  - We assume that you will use three.js, a wrapper around webGL to create your VR project.
      You can find some great docs for three.js here: http://threejs.org/docs/
  - Always Remember: Google is your friend!
3a. OR change index.html to point at blankWebVR.js in the webVR-boilerplate/js folder and create your scene from scratch
  - blankWebVR.js contains no sample code, but you can always cross reference demoWebVR.js if you would like some

Bonus: Set up your computer to serve up your website to localhost, this allows you to do things like experiment with image and video textures and test-run your stuff on your mobile device. The fastest and simplest is probably python simple server (default port is 8000):

% python -m SimpleHTTPServer [port]

# Acknowledgements
This boilerplate is based on [Mozilla's boilerplate](https://github.com/MozVR/vr-web-examples/tree/master/threejs-vr-boilerplate)

It has been developed with the advice, help, and contributions of a great many people including (but not limited to) the other members of the eleVR team (Emily Eifler and Vi Hart), [Andrew Lutomirski](https://github.com/amluto), and Henry Segerman.

