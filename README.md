# QtTrafficSim

**QtTrafficSim** (*EasyRider*) is an interactive traffic simulator written in C++ using the Qt framework. The application allows for real-time visualization and control of traffic parameters, simulating vehicle behavior, traffic lights, and interactions between road users.

## Table of Contents
1. [Project Description](#project-description)
2. [Features](#features)
3. [Technologies](#technologies)
4. [Screenshots](#screenshots)
5. [Installation and Compilation](#installation-and-compilation)
6. [Project Structure](#project-structure)

## Project Description

The goal of the project is to simulate a simple road system. The application manages the lifecycle of vehicles, their movement on a designated road map (a graph of streets and intersections), and their reaction to the environment, such as other vehicles or traffic lights. The user can influence the simulation via a control panel.

## Features

*   **Real-time simulation:** Smooth rendering of vehicle movement.
*   **Traffic control system:** Support for intersections and traffic lights (`TrafficLight` class).
*   **Intelligent vehicle behavior:**
    *   Collision detection and maintaining safe distance.
    *   Vehicles implemented as state machines: Driving (`DrivingState`), Stopped (`StoppedState`), Following another vehicle (`FollowingState`).
*   **GUI Control Panel:**
    *   Start/Pause simulation.
    *   Slider for vehicle limit on the map.
    *   Slider for vehicle spawn frequency (Spawn Rate).
    *   Slider for simulation speed.
*   **Map management:** A system based on nodes (`StreetMapNode`) and streets (`StraightStreet`), creating a coherent road network.

## Technologies

The project was implemented using the following technologies:

*   **Language:** C++17
*   **GUI Framework:** Qt (Qt5 / Qt6 - Widgets)
*   **Build System:** CMake (minimum version 3.5)

## Screenshots

<img width="1002" height="739" alt="image" src="https://github.com/user-attachments/assets/0b085884-f77d-458b-8b0c-498ab0f33a03" />
*Main simulation view*

## Installation and Compilation

To compile and run the project, you need a C++ compiler, CMake, and Qt libraries.

### Prerequisites
*   C++ Compiler (GCC, Clang, MSVC) supporting C++17
*   CMake
*   Qt 5 or Qt 6 (`Widgets` module)

### Installation Steps

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/jakub-cz01/QtTrafficSim.git
    cd QtTrafficSim
    ```

2.  **Create a build directory:**
    ```bash
    mkdir build
    cd build
    ```

3.  **Configure the project using CMake:**
    ```bash
    cmake ..
    ```

4.  **Compile the project:**
    ```bash
    cmake --build .
    ```

5.  **Run the application:**
    On Linux/macOS:
    ```bash
    ./EasyRider
    ```
    On Windows:
    ```bash
    Debug\EasyRider.exe
    ```

## Project Structure

Main files and classes in the project:

*   **`main.cpp`**: Application entry point.
*   **`mainwindow.cpp/h`**: Main window and user interface handling.
*   **`simulationloop.cpp/h`**: Main loop controlling simulation logic (Singleton pattern).
*   **`vehicle.cpp/h`**: Class representing a vehicle.
*   **`vehiclemanager.cpp/h`**: Managing vehicle creation and deletion.
*   **`trafficlight.cpp/h`**: Traffic light logic.
*   **`streetmap.cpp/h`**: Road map representation.
*   **`*.ui`**: Qt Designer user interface files.

---
Author: [jakub-cz01](https://github.com/jakub-cz01)
