# RPi_Obj_Detection
Trained object detection model which can be easily deployed on RPi. This model is trained on UK license plates.
This code will record clips where the object is detected and save them to your current directory with timestamp of when clip was captured.

![image](https://user-images.githubusercontent.com/64171887/191074347-a84de26b-cca7-4b08-942a-c478709a7703.png)

![image](https://user-images.githubusercontent.com/64171887/191074567-902b0fba-c82a-4606-83ed-7652ca68480a.png)

# Tensorflow Object Detection Walkthrough with Raspberry Pi
<p>The following repository will allow you to leverage Tensorflow Object Detection models that have been converted to TFLite on a Raspberry Pi.
## Steps
<b>Step 1.</b> Walk through the object detection tutorial by Nick Nochnack and generate the TFlite files. The important one is the .tflite file. https://github.com/nicknochnack/TFODCourse
<br/><br/>
<b>Step 2.</b> Clone this repository onto your Raspberry Pi or copy it from a machine using RDP.
<b><br/>Step 3.</b>Install the required dependencies onto your Raspberry Pi
<pre>
pip3 install opencv-python 
sudo apt-get install libcblas-dev
sudo apt-get install libhdf5-dev
sudo apt-get install libhdf5-serial-dev
sudo apt-get install libatlas-base-dev
sudo apt-get install libjasper-dev 
sudo apt-get install libqtgui4 
sudo apt-get install libqt4-testv
echo "deb https://packages.cloud.google.com/apt coral-edgetpu-stable main" | sudo tee /etc/apt/sources.list.d/coral-edgetpu.list
curl https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key add -
sudo apt-get update
sudo apt-get install python3-tflite-runtime OR if on normal linux machine python3 -m pip install tflite-runtime
</pre>
<b>Step 4.</b> Copy your detect.tflite model into the same repository and update the labels.txt file to represent your labels. 
<br/>
<b>Step 5.</b> Run real time detections using the detect.py script
<pre>python3 detect.py</pre>
<br/>

![image](https://user-images.githubusercontent.com/64171887/191074174-b1a718ed-d225-4b7d-a304-12b69b682726.png)

