## ROS 2 Add Two Integers - Server and Client
This repository demonstrates a simple implementation of a server-client interaction in ROS 2. It features a service-based interaction where the client sends two integers, and the server responds with their sum.

## Features
### Add Two Integers Service:
The server node listens for requests on a custom service, adds two integers, and returns the result.
The client node sends two integers to the server and receives the sum.

### Implemented in Both Python and C++:
Python nodes using rclpy.
C++ nodes using rclcpp.

## Prerequisites
ROS 2 Installation: ROS 2 (Jazzy) is installed on Ubuntu 24.04 distribution.
Development Tools: Necessary build tools like colcon for building the packages.

## Installation
1. Clone the Repository:
   
mkdir -p ~/ros2_ws/src

cd ~/ros2_ws/src

git clone https://github.com/khanhhado1208/Simple-Template-Server-Client-ROS2.git

2. Build the Packages:
   
cd ~/ros2_ws

colcon build

3. Source the Setup Script:
   
source install/setup.bash

## Running the Python Nodes
1. Start the Service Server:
   
ros2 run my_python_pkg add_two_ints_server

2. tart the Service Client (in a new terminal):
   
ros2 run my_python_pkg add_two_ints_client_oop

3. Test with a Command Line Call:
   
ros2 service call /add_two_ints example_interfaces/srv/AddTwoInts "{a: 5, b: 10}"


## Running the C++ Nodes
1. Start the Service Server:
   
ros2 run my_cpp_pkg add_two_ints_server

2. tart the Service Client (in a new terminal):
   
ros2 run my_cpp_pkg add_two_ints_client

3. Test with a Command Line Call:
   
ros2 service call /add_two_ints example_interfaces/srv/AddTwoInts "{a: 5, b: 10}"

## ROS2 Concept
Services

Service Name: /add_two_ints

Service Type: example_interfaces/srv/AddTwoInts

Request: Two integers (a, b).

Response: Their sum.

## Commands to Explore
1. List Available Services:

ros2 service list

2. Check the Service Type:
ros2 service type /add_two_ints

3. Inspect the Service Definition:
   
ros2 interface show example_interfaces/srv/AddTwoInts

### Demo Video:
[[click here]([www.google.com](https://www.youtube.com/watch?v=679Axf3pNbk))](https://www.youtube.com/watch?v=679Axf3pNbk)
