---
layout: page
title: "The Aesthetic and Structural Innovation of Robotic Bodies"
date: 2026-07-06
---

The Aesthetic and Structural Innovation of Robotic Bodies 

David Jian Tang, Smart Line Robotic Inc., Raleigh, NC27604, USA. 

Yiping Tang,School of Computer Science,Hunan Normal University, Changsha, Hunan Province, China.

Sheng Rao, Cornell University, USA；University of South Florida，Tampa, Florida, USA.

May 20, 2026


Abstract
This paper proposes a novel robotic body based on a nonlinear scissor mechanism with forward bending and gradient link lengths. By introducing a non-uniform geometric configuration into the conven[...]


Index Terms
Nonlinear scissor mechanism, robotic structure, kinematics, telescopic arm, robotic design


I. Introduction
Robotic manipulators are widely used in industrial automation, medical systems, rehabilitation, and service industries. With the rapid integration of artificial intelligence and physical systems, [...]

B. Conical Telescopic Arm
The arm is composed of multiple scissor units and a semi-scissor unit connected in series:
Each scissor unit consists of two hinged links
Adjacent units are connected via pivot joints
The semi-scissor unit provides terminal constraint
Key structural characteristics include:
Link lengths decrease monotonically from base to tip
Each link exhibits forward bending
Bending angles vary gradually along the arm
The entire structure forms a conical topology (0°–80°)


C. Kinematics and Inverse Kinematics
Unlike traditional articulated robots, whose kinematics are highly nonlinear, experimental results reveal that the proposed structure exhibits an approximately linear mapping between input and out[...]


This linearization significantly reduces computational complexity, enabling high-precision control using low-cost controllers.
Further analysis indicates that:
The average transmission ratio ≈ 512.7
Local transmission ratio increases with stroke
This non-uniform amplification behavior is attributed to the conical gradient geometry, which improves load distribution and mechanical efficiency.
The simplification of robot kinematic equations and inverses simplifies the robot control system, thereby enhancing the robot's computing power.


D. Experimental Setup and Validation
Prototype specifications:
Arm length: 3.5 m
Payload: 25 kg
Actuation: electric cylinder with encoder feedback
Experimental data confirm:
Near-linear displacement mapping
Increasing local transmission ratio along extension
This phenomenon demonstrates that structural symmetry leads to simplified kinematics despite geometric complexity.


III. Working Principle
The robot operates by actuating relative motion between adjacent scissor units, resulting in synchronized extension or contraction.
Key characteristics:
Linear motion output
Triangular support-like stability
Wide base for stiffness
Narrow tip for confined workspace
The actuator stroke is only 5%–10% of total extension, significantly reducing actuator size and system cost.


IV. Advantages
1) High Stability and Load Capacity
The conical symmetric structure enhances rigidity and load-bearing capability.
2) Ultra-Low Energy Consumption
Compared with conventional robots requiring kilowatt-level motors, the proposed system operates at approximately 50 W, due to:
Planar motion (no gravity compensation)
Reduced rotational inertia
3) No Precision Reducers Required
Eliminates ~40% of robot cost associated with reducers.
4) Simplified Control Algorithms
Linear kinematics enable accessibility even for low-level developers, greatly expanding adoption.
5) Robots of different sizes and shapes can be constructed in a modular fashion. 
Single scissor-type modules can be connected in series or parallel to construct various types of robots, even heavy duty robots. For example in Fig.3, It used less scissor-type modules to constru[...]

Fig.5 Compact robot
6）Construct multiple hands on long arm robot
Install one or more wrist robots on the end of a long-arm robot or different place of it for various applications as Fig.6.


V. Conclusion
This paper presents a nonlinear gradient scissor-based robotic arm with a conical topology. The design overcomes the fundamental limitation of traditional scissor mechanisms and simplifies the co[...]
The system achieves:
Stable extension
High payload capacity
Low energy consumption
Simplified control
Future work will explore additional nonlinear scissor configurations, including spherical, ellipsoidal, cylindrical, and modular forms, enabling a wide range of robotic applications.


References
[1] Q. Wang, Design and Analysis of Industrial Manipulators, 2014.
[2] Y. Li and Z. Chen, “Low-cost design of joint robots,” Manufacturing Systems, vol. 35, pp. 89–96, 2015.
[3] H. Zhang, “Heavy-duty telescopic manipulators,” Journal of Mechanical Engineering, vol. 50, no. 11, pp. 1–8, 2014.
[4] J. Craig, Introduction to Robotics: Mechanics and Control, 3rd ed. Beijing: China Machine Press, page101, 2019.
[5] J. D. Smith and A. M. Johnson, “Scissor mechanisms in engineering,” J. Mechanical Design, 2018.
[6] Y. Li et al., “Deformation characteristics of scissor trusses,” JCSR, 2020.
[7] R. Garcia and J. Martinez, “Telescopic structures for aerospace,” Acta Astronautica, 2019.
[8] W. Chen et al., “Cube-like modular structures,” Construction Materials, 2021.
[9] T. Brown and S. Davis, “Intelligent telescopic structures,” IEEE/ASME Trans. Mechatronics, 2022.
