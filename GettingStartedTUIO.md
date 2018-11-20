Hello Language Teaching Aficionados,

TUIO will do what you want in realtime with something like QR codes.  It can detect many fiducials at the same time and much more, if needed.  TUIO (Tangible User Interface Object) is an open protocol for the communication of data from devices like a multi-touch display, an interactive surface, or a computer vision-based motion tracker.  While it introduces more complexity, the good news is that the front end image processing is a standalone program and there is a Processing backend that you can simply tweak to add sound and implement your specific design.

Get inspired by what TUIO can do:
TUIO comes from the technology that underlies this multitouch tangible user interface table called Reactable
https://www.youtube.com/watch?v=Mgy1S8qymx0 (this table uses the exact same fiducials and protocol and has been used live by Bjork)

Think of it as an iPad... but drastically larger in surface area, capable of hundreds of objects and touches, and drastically cheaper than an iPad.  Oh, and you just need Processing to program, not Swift or Objective-C for iOS.

Overview:
The links below are from the TUIO main site that introduces the system in much more detail http://reactivision.sourceforge.net/  This would be good to check out to understand the context and what options there are for using the TUIO protocol.  

How to Make it Work:
Spoiler: steps 1-2 should take less than 5 minutes.
1) Download the frontend video processing, called reacTIVision, for mac:
http://prdownloads.sourceforge.net/reactivision/reacTIVision-1.5.1-mac64.zip?download

2) After downloading, run reacTIVision and hold an image of one of the below fiducials in front of the camera.  The black and white video image should detect known fiducial images by superimposing a light green number corresponding to the fiducial id.  If you open and hold up the below image of 6 fiducials in front of your camera, reacTIVision should detect up to 6: 
I took this screen shot of it working.  Notice the green numbers that show the unique id.  This is just my phone displaying the above image in front of the camera while running reacTIVision

This proves that you can detect specific fiducials from reacTIVision.  For your project, the fiducials can just be printed and stuck to the bottom of your letters.

Spoiler: 3-5 should only take another 5 minutes.
3) Download the backend and install the libraries into Processing.  The backend takes the detected input from reacTIVision and does something with it.  There are demos that you can build on:
(You must install this library into Processing following the *manual* process here https://github.com/processing/processing/wiki/How-to-Install-a-Contributed-Library)
http://prdownloads.sourceforge.net/reactivision/TUIO11_Processing-1.1.5.zip?download

4) Connect frontend to backend: make sure reacTIVision is running and then, in Processing (assuming you installed the library correctly), open File>Examples>Contributed Libraries>TUIO>"TuioDemo".  Run this sketch by clicking the "Play" button.

5) Processing's view is a distillation of reacTIVision.  You should just see black boxes with unique ids representing the fiducials that are detected in front of your camera.  You will just see a white screen until you hold up fiducials in front of the camera again.
This is a screen shot of Processing TuioDemo detecting the same fiducials as above.

..Now you're ready to program your specific design.  This will probably take more than 5 minutes.
6) The next step is to program in Processing.  You'll want a specific sound to play when a consonant is detected.  Possibly you'll want to program when a correct word is complete and then play the full word.  To do this, you'll need to understand where to make changes in the TuioDemo code.  We can talk about this on Tuesday.  

We're jumping into the deep end here and RFID or other approaches are still good options if this seems overly complex.  Please let me know if you have any questions.  
