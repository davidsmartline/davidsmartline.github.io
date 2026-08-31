We are creating AI-related jobs and offering AI vocational training. Through these practical courses, we teach you how to train, manage, and maintain robots, as well as how to generate, clean, and annotate data. In this way, we help you master AI and become part of the AI ​​workforce. These are the course materials for our first lesson.

Introductory AI / Machine Learning Laboratory with Robot

— Understanding “Data → Model → Training → Testing → Deployment” with a One-Axis Long-Reach Robot

Intended for: College / Polytechnic Students and AI Beginners
Revised Edition · August 2026

1. Course Positioning and Learning Objectives
This laboratory does not begin with complicated neural-network equations. Instead, students first operate a real robot, collect data by themselves, and then use a simple supervised-learning model to perform training and prediction. In this way, students can directly understand one of the most important workflows in artificial intelligence: Data → Model → Loss Function → Training → Testing → Deployment.
Strictly speaking, this experiment uses univariate linear regression in supervised learning. It is a fundamental machine-learning model rather than a deep-learning model. Once students understand this complete learning process, the transition to multilayer neural networks and deep learning becomes much easier.
•	Understand the meanings of input x, output y, model parameters, predicted values, and measured values in supervised learning.
•	Operate a real robot and collect a set of training data.
•	Understand the loss function (MSE) and the idea that training means finding parameters that minimize the loss.
•	Use Python to calculate the model parameter and test the model with new data.
•	Develop an initial understanding of training sets, test sets, underfitting, overfitting, and model deployment.
2. Core Concept: Starting with the Simplest Model
The basic task of supervised learning is to use a set of known input-output pairs (xᵢ, yᵢ) to learn a model that can make a reasonable prediction ŷ for a new input x.
In this experiment, we first use a one-variable linear model constrained to pass through the origin:
ŷ = kx
where x is the commanded displacement of the robot’s linear actuator; y is the measured displacement of the robot end point; ŷ is the model-predicted end-point displacement; and k is the model parameter to be learned from data.
For the i-th sample, the prediction error is eᵢ = yᵢ − ŷᵢ. To measure the overall prediction error of the model, we use Mean Squared Error (MSE):
L(k) = (1/n) Σ (yᵢ − kxᵢ)²
The objective of model training is to find the value of k that minimizes the loss L:
k* = arg minₖ L(k)
Note: If actual measurements show that y is not close to zero when x = 0, the model can be extended to ŷ = kx + b, in which both the slope k and intercept b are learned.
3. Experimental Robot
The experimental platform is a one-axis long-reach robot driven by a linear actuator and based on a nonlinear scissor mechanism. An important feature for this laboratory is that, within the selected operating range, the actuator displacement x and robot end-point displacement y have an approximately linear relationship. This makes the system particularly suitable for beginners learning supervised learning and model fitting with a real physical machine.
The original course material lists example robot specifications of approximately 3 m reach and 48 W drive power. The purpose of this laboratory, however, is not to validate those performance specifications, but to learn how to acquire data from a physical robot and build an input-output model.
 
Figure 1. One-axis long-reach robot used in the experiment (photo from the original course material)
4. Experimental Environment and Safety
4.1 Software and Hardware
•	Arduino Mega (or the controller board specified by the laboratory) and a USB cable.
•	Arduino IDE: used to upload/run the controller program and communicate with the board through the Serial Monitor.
•	Python 3: used for data processing, model training, plotting, and prediction. VS Code, IDLE, Jupyter Notebook, or a teacher-preconfigured environment may be used.
•	Robot, linear actuator, displacement measurement tools, and the Arduino control program and Python training program supplied by the instructor.
Important correction: A .py file is a Python program and should not be run in the Arduino IDE. The Arduino IDE runs the controller-side program, while AILearning.py should be run in a Python environment.
4.2 Safety Requirements
•	Before powering the robot, confirm that the working area is clear of people and obstacles and that the emergency-stop function is available.
•	For the first motion test, use low speed and a small displacement. Before each command, confirm that the requested motion is within the allowable travel range.
•	Keep hands away from pinch points in the scissor mechanism, guide rails, and linear actuator.
•	If abnormal noise, jamming, uncontrolled motion, or communication failure occurs, press the emergency stop immediately and inform the instructor.
•	Students must not modify motor-drive, power-supply, or limit parameters without authorization.
5. Experimental Procedure
Step A: Connect the Control System
1.	Install the Arduino IDE and connect the Arduino Mega to the computer using a USB cable.
2.	In the Arduino IDE, select the correct Board and Port under the Tools menu. The port may appear as COM3, COM4, etc.; use the port actually detected by the computer.
3.	Open and upload the Arduino control program supplied by the instructor. After uploading, the Serial Monitor may be opened for communication tests.
4.	Start the Python environment and open AILearning.py. If the Python program needs to access the serial port, close the Arduino Serial Monitor first so that two programs do not attempt to use the same serial port simultaneously.
 
Figure 2. Example Arduino IDE interface (screenshot from the original course material)
Step B: Collect Robot Data
Command the linear actuator sequentially using the assigned x values and measure the actual displacement y of the robot end point. It is recommended to repeat each measurement two or three times and use the average value to reduce human measurement error.
No.	x: Actuator Displacement (mm)	y₁ (mm)	y₂ (mm)	Average y (mm)
1	0			
2	20			
3	40			
4	60			
5	80			
6	100			
7	120			
8	140			
9	160			
10	180			
11	200			
12	220			
13	240			
14	250			
Recommendation: Do not keep only the data set that “looks best.” Small errors in real measurements are part of a machine-learning experiment. If a data point is clearly abnormal, record the reason instead of simply deleting it.
Step C: Divide the Data into Training and Test Sets
To determine whether the model can predict data that were not used during training, divide the measurements into a training set and a test set. For example, every fourth data point may be reserved for testing, while the remaining points are used for training. For a first introductory exercise, the entire data set may be fitted initially, followed by a second exercise introducing the training/test split.
Step D: Train the Model
Enter the training data into the Python program. The program evaluates the loss L(k) for different values of k and finds the value k* that minimizes the MSE. If the model is restricted to ŷ = kx, the least-squares solution can also be calculated directly:
k* = Σ(xᵢyᵢ) / Σ(xᵢ²)
Using the example data in the original course material, the fitted slope is approximately k = 7.8109. The example model is therefore:
ŷ = 7.8109x
The value 7.8109 is obtained by fitting the example data. Students may obtain a slightly different k from their own measurements; this is normal in a real experiment.
Step E: Test and Evaluate the Model
Select x values that were not used for training. First let the model predict ŷ, then command the robot and measure the actual value y. Compare the prediction with the measurement and calculate the test error.
Test x (mm)	Predicted ŷ (mm)	Measured y (mm)	Absolute Error |y−ŷ|	Relative Error (%)
				
				
				
				
If both the training error and test error are large, the model may be too simple; this is called underfitting. If the training error is very small but the test error is significantly larger, the model may have learned details specific to the training data and may generalize poorly; this is related to overfitting. For this one-variable linear experiment, the objective is to understand these concepts rather than deliberately build a complicated model.
Step F: Model Deployment — Using the Learned Model to Control the Robot
After training, the model can do more than predict the end-point displacement y from an input x. When k ≠ 0, it can also be approximately inverted:
x ≈ y_target / k
For example, if a desired end-point displacement y_target is specified, the model can first calculate the required actuator displacement x, after which the control program executes the command. Students have then completed a small but complete “AI / Machine Learning + Physical Robot” closed loop: Data Collection → Model Learning → Prediction → Control → Physical Measurement and Verification.
6. Questions for Discussion
5.	Why is it not enough to evaluate only the error on the training data? What is the purpose of test data?
6.	If all measured points lie exactly on a straight line, is a large amount of training data still necessary? Why?
7.	If different robot loads produce different values of k, how could the model be extended by adding input variables?
8.	If the relationship between x and y is clearly nonlinear, how should the model be changed?
9.	What does this experiment have in common with a real deep neural network? What are the major differences?
7. Laboratory Report Requirements
•	Record the experimental setup, software environment, and safety checks.
•	Submit the original x-y measurements, not only the fitted result.
•	Plot a scatter graph of the measurements and draw the fitted line obtained from training.
•	Report the model, parameter k, training MSE, and test error.
•	In 100–200 words, explain the relationship among data, model, loss function, training, testing, and deployment.
•	Identify at least one source of experimental error and propose one method for improvement.
8. Summary
The purpose of this laboratory is not to ask beginners to start immediately with complicated deep neural networks. Instead, it uses a real robot to take students through the complete logic of machine learning: the physical world produces data; a model describes the relationship between input and output; a loss function measures prediction error; training finds better model parameters; testing evaluates the model on new data; and finally the learned model is deployed back to the robot.
On this foundation, later laboratory courses can progressively introduce multiple input variables, nonlinear models, neural networks, vision and force-sensing data, and more complex robot-control tasks, providing a natural transition to deep learning and embodied/physical AI.
