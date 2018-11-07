# Autonomous Car

Driverless miniature car powered by 3D Camera, LiDAR and Game Controller connected to the Jetson TX2 Board. ROS is installed on Ubuntu running on the TX2 and massaging of the frames captured by the camera is done using OpenCV. This data is sent over to the 5 node HDP3.0 Cluster running on AWS. YARN is used to spin up Zeppelin container to use tensorflow to create the model, train the model and send it back to the car for testing. If the car is able to move around the track and avoid obstacles, then the model is well trained, else the model is sent back to the HDP3.0 cluster for train debugging. Once retrained, the model is sent back to the car for testing again. By using the LiDAR data, camera data and GPU inference, the model converts the car captured images of the track to steering angles, so the car can drive autonomously.

![mini-car.jpg](assets/images/mini-car.jpg)

![controller.jpg](assets/images/controller.jpg)
