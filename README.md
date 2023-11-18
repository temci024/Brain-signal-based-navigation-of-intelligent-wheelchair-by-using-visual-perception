# Brain-signal-based-navigation-of-intelligent-wheelchair-by-using-visual-perception

### Final Year Undergraduate Project 2023
#### Electrical Engineering Department
#### University Of Moratuwa


## Team Members:
- D.J.Temcious.Fernando
- Apisaruthan Thanabalasingam
- Sobikanth Mahendran

## Supervisors:
- Prof. A.G.B.P. Jayasekara, Faculty of Engineering, Department of Electrical Engineering
- Prof. R.A.R.C. Gopura, Faculty of Engineering, Department of Mechanical Engineering

## Problem Statement:
Individuals with spinal cord injuries or paralysis, despite having a healthy brain and vision, face a significant
challenge in independently navigating their wheelchairs in known environments. The inability to utilize their
hands and legs for wheelchair control hinders their mobility and independence, necessitating constant reliance
on others for movement. This dependence on external assistance limits their ability to explore and navigate
their surroundings freely. Consequently, there is a pressing need to develop innovative solutions that empower
these individuals to regain control over their wheelchair navigation.

## Conceptualization:
The process of navigating a wheelchair using Steady State Visual Evoked Potential (SSVEP) brain signals involves
a specific mechanism. When a person focuses their attention on a flickering light that operates at a particular
frequency, a corresponding frequency signal is generated in their brain. This signal is known as the SSVEP brain
signal.
The SSVEP brain signal can be extracted from the brain using appropriate techniques and converted into a
control signal. In a known environment, if a patient wishes to navigate from their current location to another
location, they can provide control commands to the wheelchair using their brain-generated control signal.
By utilizing the extracted control signal, the wheelchair can autonomously navigate from the current location to
the specified location without the need for external assistance. This eliminates the requirement for another
person to physically move the wheelchair, providing the patient with greater independence and freedom of
movement.

## System Overview:
he system is divided into two major sections: brain signal processing and automatic wheelchair navigation.
In the brain signal processing section, a user interface is created, consisting of four flickering frequency squares.
Each frequency corresponds to a different location within the known environment. The brain signal is acquired
using a brain signal acquisition system. It undergoes preprocessing, feature extraction, and classification
techniques to convert it into a control signal.
The processed control signal serves as input for the wheelchair navigation section, allowing the wheelchair to
autonomously navigate to the specified location within the known environment.

![simulationModel_new_final (1) drawio](https://github.com/temci024/Brain-signal-based-navigation-of-intelligent-wheelchair-by-using-visual-perception/assets/129023792/07546627-d9ac-442b-9d1d-cf406f0cf1bb)


## Results :
In the experiment, brain signals corresponding to frequencies of 6 Hz, 7 Hz, 8 Hz, and 9 Hz were successfully
extracted and converted into control signals. The brain signals, obtained in real-time from the subjects,
underwent signal processing and classification to accurately identify the frequencies of interest.
By mapping these frequencies to specific navigation commands, the control signals were generated. These
control signals were then utilized for automatic navigation of a robot model using ROS2 in a simulation
environment.

![result](https://github.com/temci024/Brain-signal-based-navigation-of-intelligent-wheelchair-by-using-visual-perception/assets/129023792/fa717d50-02bc-4c34-a21a-e081f48ad2eb)

<p align="center">Figure 01: Extracted brain signals after preprocessing.</p>



![gazeboSimulation](https://github.com/temci024/Brain-signal-based-navigation-of-intelligent-wheelchair-by-using-visual-perception/assets/129023792/aa80f306-4e9b-4f2e-97b5-a699c4503c79)

<p align="center">Figure 02: Real-time automatic navigation of the robot in the simulation environment using
Gazebo and Rviz platforms based on the detection of the 7 Hz frequency signal, leading to the
selection of the corresponding location.</p>


The implementation of this idea directly into the wheelchair itself has not been realized yet, primarily due to hardware limitations. 
However, an alternative approach has been adopted by activating simple controls on the wheelchair. This is achieved through real-time classification of brain signals, bypassing the
traditional joystick and utilizing an Arduino Micro controller. Each classified brain signal is assigned to a
specific path, enabling real-time navigation of the wheelchair along predefined routes

