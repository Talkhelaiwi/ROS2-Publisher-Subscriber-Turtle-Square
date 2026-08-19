# ROS2 Publisher Subscriber & Turtle Square

## Description

This project demonstrates basic ROS 2 concepts using Python.

The project includes:

* A **Publisher (Talker)** that sends a custom message instead of "Hello World".
* A **Subscriber (Listener)** that receives and displays the published message.
* A **Turtlesim controller** that moves the turtle in a square path instead of a circle.

## Requirements

* Ubuntu 22.04
* ROS 2 Humble
* Python 3
* Turtlesim

## Part 1: Publisher and Subscriber

The publisher sends the following custom message:

```text
Smart Methods Task
```

The subscriber receives and displays the message:

```text
I heard: "Smart Methods Task"
```

### Run the Publisher

```bash
source /opt/ros/humble/setup.bash
source ~/ros2_ws/install/setup.bash
ros2 run py_pubsub talker
```

### Run the Subscriber

Open another terminal and run:

```bash
source /opt/ros/humble/setup.bash
source ~/ros2_ws/install/setup.bash
ros2 run py_pubsub listener
```

## Part 2: Turtle Square Movement

The Turtlesim code was modified so that the turtle:

1. Moves forward.
2. Turns 90 degrees.
3. Repeats the movement four times.
4. Stops after completing the square.

### Run Turtlesim

```bash
source /opt/ros/humble/setup.bash
ros2 run turtlesim turtlesim_node
```

### Run the Square Controller

Open another terminal:

```bash
source /opt/ros/humble/setup.bash
source ~/ros2_ws/install/setup.bash
ros2 run turtle_square square
```

After completing the square, the terminal displays:

```text
Square completed!
```

## Result

The Publisher and Subscriber successfully communicate using a custom message, and the Turtlesim turtle successfully moves in a square path.

## Project Structure

```text
ros2_ws/
└── src/
    ├── py_pubsub/
    │   └── py_pubsub/
    │       ├── publisher_member_function.py
    │       └── subscriber_member_function.py
    │
    └── turtle_square/
        └── turtle_square/
            └── square.py
```

## Screenshots

### Publisher and Subscriber

![Publisher and Subscriber](images/publisher_subscriber.png)

### Turtle Square

![Turtle Square](images/turtle_square.png)
