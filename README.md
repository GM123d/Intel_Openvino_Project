# Intel_Openvino_Project
In this project I have made protype car using various hardware component (Raspberry pi, PI Camera, Motors, wire etc.). The main purpose of this project is to solve various transportation issues. For transportation purpose one always need to depend upon on the man power and one should be present at location physically. But what if we remove that limitation and make the transportation remote control with driver assistant. This will also lead to decrease in death rates of driver as our vehicle is driverless.


So, in this project I have made a simple website through which one can control its transport. there will be live feed from the camera using pi camera. I am sending the live feed from the camera using flask server. 


So what is the role of open vino in this project.

For drive Assistant part i have used openvino project. Using Object detection of tensorflow I am detecting the object in real time. It will help driver to get full insight of the environment and object around it and he/she can make proper decision.


So, how openvino is benefiting my project?

Actually as I am sending the photo on cloud and if I upload my modal on cloud and then use it for the live feeding there will be huge latency.
So if I use Openvino and move my model near to the application I can reduce this latency drastically. This is how Openvino is adding advantage to my project.


So How to run my project.

Firstly you have to import the respective files to run various files these are:- (Flask,RPI.GPO (for integration with raspberry Pi)) 
Actually to integrate the Pi Cam you will require a Camera.py file that i have include in my project.
In this repository I have not able to upload the bin file for the object detection as it too large but you can download it from open vino site as I have used the pre trained model of openvino for my project.
the name of the files will be as follows:
frozen_inference_graph.xml and frozen_inference_graph.bin
for this I have use the same object model taught in the course. 

Now for my website:-

For this we have to install node and here we will be using express framework.
all the libraries that need to be install is given in the file package.json under the section dependencies.
Here I have work mainly on backened so You will find My UI/UX not that attractive but this is because it is a protype only.
Now what are all the files for our Rasperry pi and websites.
RaspberryPi (all files except nodejs folder) (you have to install openvino on the raspberry pi to run these)
website (only nodejs folder)


Now how to run my project:-

Under the folder Camera_code there is file named camera_route.py this a file that contain the openvino code. Here check the CPU_Extension I have provided according to your openvino version and OS you have to change it.
Now to run the whole project you have to run three files:-
python_code.py
camera_route.py (under folder camera code) (running this file you have to provide the path of your models xml file through command prompt)
for installing openvino on raspberry pi ypu can
app.js (under folder nodejs)
Here in this python_code.py and camera_code.py I have defined the port So while running You have to free those port or change the code according to your free ports.


When all of this is done. you can see when you run your app.js file your website will be open and you can see a input box .
In that input box you have to specify the ip address of your Raspberry pi and then click on submit.
Now if everything’s is done properly you will see live feed from the camera and object are being detected in it and below that there are controls to control your car.


Limitations of my project.

for this to implement in the real life one should need a private network whose reach is available all over the world which is very costly.


Future aspects of my project.

You can advance it to self driving concept.
In this I have done object detection only but you can extend the idea to Lane detection distance between vehicles and give proper insight to the driver to make good decision. Then this software will act as good driver assistant.


In this I have attached the image of my website with real time feed through the camera it is also detecting the objects.
