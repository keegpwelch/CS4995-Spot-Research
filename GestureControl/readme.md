# CS4995 Spot Research

*Keegan Welch*  
*Fall 2021*  
*Dale Musser Research*  
*Univ. of Missouri*

### Gesture Control
Worked on the Gesture Control project with Ryan Orf and David Hannan to create a program
which implements hand gesture recognition with OpenCV and relays corresponding movements
to Spot with the Spot API. Still continuing to develop Spot movements and improve on our
implementation.

#### Running the Program
This program contains many of the same dependencies as found in the Spot-SDK, follow installation instructions [here](https://dev.bostondynamics.com/docs/python/quickstart).  

As well as other packages including numpy, OpenCV, tensorflow, and mediapipe. In a Python virtualenv:
```
$ pip install numpy
$ pip install opencv-python
$ pip install tensorflow
$ pip install mediapipe
```
In order to run the program, you must first connect to Spot's wifi and run the estop example found in the SDK.
in `spot-sdk/python/examples/estop` with your virtualenv activated:
```
$ python -m pip install -r requirements.txt

$ python estop_nogui.py --username USER --password PASSWORD ROBOT_IP
```
Then in a separate terminal, with your estop running, call the runspot.py program in the `GestureControl` directory:
```
$ python -m pip install -r requirements.txt

$ python runspot.py --username USER --password PASSWORD ROBOT_IP
```
It should then start the program and open your laptop's webcam to relay hand gesture commands to Spot.
