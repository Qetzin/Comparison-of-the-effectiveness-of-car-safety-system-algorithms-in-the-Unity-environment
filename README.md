# Master's thesis - Comparison of the effectiveness of car safety system algorithms in the Unity environment

The thesis focuses on the implementation and comparison of the effectiveness of algorithms used in car safety systems simulated in the Unity environment. The comparison will include a deterministic algorithm written using C# scripts and a machine learning model developed through the ML-Agents library. Simulation scenarios will also be designed to test different situations and conditions commonly encountered in real-world safety system tests. The results of the comparative analysis aim to distinguish the features of the presented solutions and determine which one is better suited for implementing an actual safety system.

## Link to the project
Due to the size of the project, it is stored on a disk instead of a repository. Link to the [project](https://drive.google.com/file/d/1UMA1cZN2QRbR4B8K-ZuptcVCPIkUmNvF/view?usp=sharing)

## Test scenarios
Based on the [Euro NCAP](https://www.euroncap.com/en/for-engineers/protocols/safety-assist/) documentation. 

### Car-to-Car Rear Stationary (CCRs)
Collision in which a vehicle travels 
forwards towards another stationary vehicle and the frontal structure of the vehicle 
strikes the rear structure of the other.

![](https://github.com/Qetzin/Comparison-of-the-effectiveness-of-car-safety-system-algorithms-in-the-Unity-environment/blob/main/Images/CCRs.png)

![](https://github.com/Qetzin/Comparison-of-the-effectiveness-of-car-safety-system-algorithms-in-the-Unity-environment/blob/main/Images/CCR.png)

### Car-to-Car Rear Moving (CCRm)
Collision in which a vehicle travels forwards 
towards another vehicle that is travelling at constant speed and the frontal structure 
of the vehicle strikes the rear structure of the other.

![](https://github.com/Qetzin/Comparison-of-the-effectiveness-of-car-safety-system-algorithms-in-the-Unity-environment/blob/main/Images/CCRm.png)

### Car-to-Car Rear Braking (CCRb)
Collision in which a vehicle travels forwards 
towards another vehicle that is travelling at constant speed and then decelerates, and 
the frontal structure of the vehicle strikes the rear structure of the other. 
![](https://github.com/Qetzin/Comparison-of-the-effectiveness-of-car-safety-system-algorithms-in-the-Unity-environment/blob/main/Images/CCRb.png)
### Car-to-Car Front Turn-Across-Path (CCFtap)
Collision in which a vehicle 
turns across the path of an oncoming vehicle travelling at constant speed, and the 
frontal structure of the vehicle strikes the front structure of the other. 

![](https://github.com/Qetzin/Comparison-of-the-effectiveness-of-car-safety-system-algorithms-in-the-Unity-environment/blob/main/Images/CCFTAP.png)

![](https://github.com/Qetzin/Comparison-of-the-effectiveness-of-car-safety-system-algorithms-in-the-Unity-environment/blob/main/Images/CCFtapU.png)

### Car-to-Car Crossing Straight Crossing Path (CCCscp)
Collision in which a 
vehicle travels forwards along a straight path across a junction, towards a vehicle 
crossing the junction on a perpendicular path. The frontal structure of the vehicle 
under test strikes the side of the other vehicle.

![](https://github.com/Qetzin/Comparison-of-the-effectiveness-of-car-safety-system-algorithms-in-the-Unity-environment/blob/main/Images/CCCscp.png)

![](https://github.com/Qetzin/Comparison-of-the-effectiveness-of-car-safety-system-algorithms-in-the-Unity-environment/blob/main/Images/CCCscpu.png)

### Car-to-Car Front Head-On Straight (CCFhos) 
Collision where a vehicle is 
travelling along a straight path within its defined lane and strikes another vehicle 
travelling in the opposite direction, which has drifted into the same lane as the 
original vehicle. The frontal structure of the vehicle strikes the frontal structure of 
the other. 
![](https://github.com/Qetzin/Comparison-of-the-effectiveness-of-car-safety-system-algorithms-in-the-Unity-environment/blob/main/Images/CCFHos.png)

![](https://github.com/Qetzin/Comparison-of-the-effectiveness-of-car-safety-system-algorithms-in-the-Unity-environment/blob/main/Images/CCFHOSU.png)
### Car-to-Car Front Head-On Lane change (CCFhol)

Collision where a vehicle 
is travelling along a straight path within its defined lane and strikes another vehicle 
travelling in the opposite direction which has intentionally moved into the lane of 
the original vehicle to attempt an overtake. The frontal structure of the vehicle 
strikes the frontal structure of the other.

![](https://github.com/Qetzin/Comparison-of-the-effectiveness-of-car-safety-system-algorithms-in-the-Unity-environment/blob/main/Images/CCFhol.png)

![](https://github.com/Qetzin/Comparison-of-the-effectiveness-of-car-safety-system-algorithms-in-the-Unity-environment/blob/main/Images/CCFHOLU.png)

## Testing process
The comparison of algorithm effectiveness was conducted using special enviroments designed to control two vehicles simultaneously. The cars execute the same commands based on user input data. In the event of danger, the collision detection algorithm transfers control of the car to the control algorithms. The purpose of the algorithms is to avoid collisions and bring the vehicle to a stop.  The tests will cover speeds ranging from 10 to 80 kilometers per hour.

![](https://github.com/Qetzin/Comparison-of-the-effectiveness-of-car-safety-system-algorithms-in-the-Unity-environment/blob/main/Images/SG.gif)

![](https://github.com/Qetzin/Comparison-of-the-effectiveness-of-car-safety-system-algorithms-in-the-Unity-environment/blob/main/Images/FTAPG.gif)

## Sensors
The sensors were implemented using RayCasts and 3D Box Colliders.

Due to the developed test scenarios, the car sensors will be positioned at the front of the vehicle. Sensors on the sides will not be utilized, as the tested algorithms will not respond to this type of threat.

## Scores
### Deterministic algorithm score
![](https://github.com/Qetzin/Comparison-of-the-effectiveness-of-car-safety-system-algorithms-in-the-Unity-environment/blob/main/Images/ScoreD.png)

### Machine learning algorithm score
![](https://github.com/Qetzin/Comparison-of-the-effectiveness-of-car-safety-system-algorithms-in-the-Unity-environment/blob/main/Images/ScoreAI.png)

Based on the conducted studies in specific simulated scenarios, the deterministic algorithm proved to be more effective at avoiding collisions than the machine learning algorithm, despite limitations such as lower sensor quality and limited data resources. Additionally, the deterministic solution is characterized by higher predictability and easier error traceability.

The optimal solution would involve combining both approaches to create a reliable algorithm capable of processing large amounts of data simultaneously. However, if a choice must be made between these two types of algorithms, the deterministic solution offers attributes that positively impact the performance of safety systems.




