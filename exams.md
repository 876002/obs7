# OBS7 Past Exams

## 2019Dec_OBS7_EXAM_ENfinal.pdf

### Page 1

You can answer in Dutch as well 
1 
 
This is the regular exam of OBS7 (Observers for State Space Systems) course. The exam 
duration is 100 minutes. 
It consists of the following sections, 
 
18% short answer questions. (10 mins)  
 
50% system and controller analysis questions. (55 mins)  
 
32% design question and reasoning: A control engineering problem, in which you will 
write a small report explaining the steps to achieve the found conclusions and 
controllers. (35 mins) 
The times are indicative, you can spend more time on one part and less on the other part. 
Final grade = (sum of points) / 10       with a minimum of 1.0 
Allowed tools/resources: 
Paper, Calculator, course book, Laptop/PC only using for MATLAB and Microsoft Word 
Recommendations:  
 
For long assignment answers start working with Microsoft Word, while generating your 
report. In that way, if N@tschool crashes you don't lose all your work. At the end, copy-
paste the text in Word to the textbox on N@tschool. Before you submit your exam there 
is an opportunity to submit your Matlab, Simulink, and Word files that support your 
solutions. 
 
If you need drawings and/or block diagrams to explain your ideas, use a regular exam 
paper and submit it at the end of the exam. However, the preferred option is digital 
submission.  
 
Use MATLAB notation for complicated formulae or matrices to type quicker. e.g.  
=> 10*[1 2 3; 4 5 6; 7 8 9]^2    or   10*[1, 2, 3; 4, 5, 6; 7, 8, 9]^2 
 
Make sure that any MATLAB code you submit does not contain any error. It should be 
running in one shot. If you use your premade MATLAB functions, submit a copy of the 
function itself such that your work can be run by the grader. Copying the content of 
each function at the end of the code will suffice. 
 
Choose the variable names in MATLAB so that they are understandable, for example 
A_CL to represent closed loop A matrix, instead of e.g. f7853A_kaas. 
 
The general terms and conditions of the Fontys Institute of Engineering apply to this exam.

### Page 2

You can answer in Dutch as well 
2 
 
Short answer - 1) (18 pts, 10 mins) Given the following block diagrams of control strategies 
numbered by 1), 2), 3), 4), 5), and 6) for a state space system which is described by A,B,C,D. 
1)
 
2)  
 
 
 
 
3)   
4)  
 
 
 
 
5)  
 
 
 
 
 
 
6)  
 
 
 
 
 
 
Match the most suitable names below (A to M) with the given block diagram numbers (1 to 6). There 
is a one-to-one match, hence 7 names should be left out without matching. (Example answer format: 
F-1, G-2 etc.) 
A) Full state feedback control with reference tracking  
B) 
Full state feedback control without reference tracking    
C) 
Feedforward control with full state feedback without observer 
D) Feedforward control without full state feedback with observer 
E) 
Output feedback P controller with reference tracking

### Page 3

You can answer in Dutch as well 
3 
 
F) 
Output feedback P controller without reference tracking  
G) Output feedback PI controller with reference tracking 
H) Output feedback PI controller without reference tracking 
I) 
State space open loop response without controller  
J) 
Compensator (full state feedback control using the observed states) without reference tracking 
K) 
Compensator (full state feedback control using the observed states) with reference tracking    
L) 
Observer without full state feedback control and without reference tracking    
M) Observer without full state feedback control and with reference tracking 
 
 
 
System and controller analysis - 1) (25 pts, 25 mins)  
Consider the electric circuit shown in the figure with an 
input voltage source 𝑢(𝑡) and an output current 𝑦(𝑡). 
Using the capacitor voltage and inductor current as 
state-variables, the state and output equations can be 
found as follows: 
 
 
 
a) Is the given state space system of any of the canonical forms? If yes, which one? 
b) Find the conditions relating 𝑅1, 𝑅2, 𝐶, 𝑎𝑛𝑑 𝐿 that render the system uncontrollable.  
c) When the conditions on b) are met, explain and show if the system is stabilizable. This means 
discuss if it is possible to find a state-feedback controller that stabilizes the system under the 
conditions of question b.

### Page 4

You can answer in Dutch as well 
4 
 
System and controller analysis - 2) (25 pts, 30 mins) Given the 4th order mass-spring system with wheel 
friction and the corresponding equations of motion: 
 
The system parameters are determined as  
k = 1;  
m1 = 0.5; 
m2 = 3; 
c1 = 0.1; 
c2 = 0.2; 
 
which yields the following state space system for input force to output position 𝑥1: 
𝑥̇ = [
0
0
1
0
0
0
0
1
−2
2
−0.2
0
0.333
−0.333
0
−0.067
] 𝑥+ [
0
0
2
0
] 𝑢 
𝑦= [1
0
0
0]𝑥+ [0]𝑢
 
The following Matlab program has been run to generate the graph below: 
% Response to initial condition: 
A = [0 0 1 0;   0 0 0 1;   -2 2 -0.2 0;   0.333 -0.333 0 -0.067];   
B = [0;0;2;0];  
C = [1 0 0 0];  
sys_ss = ss(A,B,C,0) 
 
K = acker(A,B,[-3+7i -3-7i -3-13i -3+13i]); 
Acl = A-B*K;    Bcl = B; 
Ccl = C;         Dcl = 0; 
sysCL = ss(Acl,Bcl,Ccl,Dcl); 
 
t = 0:0.001:6; 
[y,t,x]=lsim(sysCL,zeros(length(t),1),t,[0;0;5;-2]); 
 
figure; plot(t,y,'LineWidth',2); 
xlabel('Time (sec)'); 
ylabel('Amplitude'); 
title('Free response of the mass-spring system');

### Page 5

You can answer in Dutch as well 
5 
 
 
As you see, one might check the free response (let-go response) of an LTI state space system output 
starting from given initial conditions using this MATLAB code.  
a) Adjust the code to see the values of the actuation signal u and the output y in the same plot. 
Write down the adjusted part of the code that generates this graph and indicate where exactly 
and what you have changed in the given code. What are the maximum and minimum value of 
the actuation signal? 
 
b) Write down which poles are chosen as desired closed-loop poles in the current controller 
design. Write down what the open loop poles are for comparing purposes. Now, assume that 
the limits of the actuation are [-230; 230]. These limits come from the hardware. How would 
you change the control design strategy to stay within those limits? Explain your approach. Did 
you need to make a compromise in terms of time domain specifications like settling time, 
overshoot, and rise-time? Check the new step response and draw conclusions on the 
performance changes using the new controller. Show that the new strategy limits the 
actuation signal indeed between [-230; 230].

### Page 6

You can answer in Dutch as well 
6 
 
Design question and reasoning -1) Compensator design (32 pts, 35 mins) 
The lateral motions of a ship that is 100m long, moving at a constant velocity of 10m/sec heading 
west, are described by 
 
where,  
𝛽= 𝑠𝑖𝑑𝑒𝑠𝑙𝑖𝑝 𝑎𝑛𝑔𝑙𝑒 (𝑑𝑒𝑔)  
𝜓= ℎ𝑒𝑎𝑑𝑖𝑛𝑔 𝑎𝑛𝑔𝑙𝑒 (𝑑𝑒𝑔)  
𝛿= 𝑟𝑢𝑑𝑑𝑒𝑟 𝑎𝑛𝑔𝑙𝑒 (𝑑𝑒𝑔)  
𝑟 = 𝑦𝑎𝑤 𝑟𝑎𝑡𝑒  
For the transfer function from 𝛿 to 𝜓, 
Design a dynamic compensator 𝐷𝑐(𝑠) as described in the 
following figure that satisfies the following criteria: 
 
 
Uses the following control law 𝑢= −(5𝛽̂ −27𝑟̂ −10𝜓̂). 
 
Has the state estimator poles equal to 6 times the regulator poles. 
 
a) Give the state equations and the transfer function for the compensator 𝐷𝑐. 
b) Calculate and write down the closed-loop poles. 
c) Plot the frequency response of the compensator and draw conclusions on the high frequency 
behavior. Does the compensator have a low-pass-filter to limit the high frequency gain. If 
yes, from which frequency on does the low-pass-filter become effective and start to reduce 
the gains. If no, discuss if it is desired to have a low-pass-filter for the found compensator.

## 2020Dec_OBS7_EXAM_EN.pdf

### Page 1

You can answer in Dutch as well 
1 
 
This is the regular exam of OBS7 (Observers for State Space Systems) course. The exam 
duration is 100 minutes. 
It consists of the following sections, 
• 
15% short explanation questions. (10 mins)  
• 
15% state space basics. (15 mins)  
• 
60% controller analysis and design: A control engineering problem, in which you will 
write a small report explaining the steps to achieve the found conclusions and 
controllers. (75 mins) 
The times are indicative, you can spend more time on one part and less on the other part. 
Final grade = (sum of points) / 10+1.0        
Allowed tools/resources: 
Paper, Calculator, course book, Laptop/PC only using for MATLAB and Microsoft Word 
Recommendations:  
• 
For long assignment answers start working with Microsoft Word, while generating your 
report. In that way, if N@tschool crashes you don't lose all your work. At the end, copy-
paste the text in Word to the textbox on N@tschool. Before you submit your exam there 
is an opportunity to submit your Matlab, Simulink, and Word files that support your 
solutions. 
• 
If you need drawings and/or block diagrams to explain your ideas, use a regular exam 
paper and submit it at the end of the exam. However, the preferred option is digital 
submission.  
• 
Use MATLAB notation for complicated formulae or matrices to type quicker. e.g.  
=> 10*[1 2 3; 4 5 6; 7 8 9]^2    or   10*[1, 2, 3; 4, 5, 6; 7, 8, 9]^2 
• 
Make sure that any MATLAB code you submit does not contain any error. It should be 
running in one shot. If you use your premade MATLAB functions, submit a copy of the 
function itself such that your work can be run by the grader. Copying the content of 
each function at the end of the code will suffice. 
• 
Choose the variable names in MATLAB so that they are understandable, for example 
A_CL to represent closed loop A matrix, instead of e.g. f7853A_kaas. 
 
The general terms and conditions of the Fontys Institute of Engineering apply to this exam.

### Page 2

![Exam Page 2](images/2020Dec_OBS7_EXAM_EN_p2.png)

### Page 3

You can answer in Dutch as well 
3 
 
Short explanation - 1) (7 pts, 5 mins)   
  
 
 
 
 
 
With the above strategy, comparable with Lab2 of OBS7, one can check if the estimator, given that it 
has a stable transfer, can estimate the states stably based on the inputs and outputs of the plant. 
Would the chosen desired observer poles’ locations have any influence on the saturation of the 
actuator, which is actuated by the signal 𝑢 (left side of the figure)? Explain your answer.  
 
Short explanation - 2) (8 pts, 5 mins)   
What is the underlying idea behind choosing faster observer poles than regulator poles?

### Page 4

You can answer in Dutch as well 
4 
 
State space basics - 1) (15 pts, 15 mins)  
Given the block diagram below for an nth order plant, where the integrator outputs are chosen as the 
states. 
 
a) Write down the B and C matrices of the state space description for the given form. (10 pts) 
b) Is this given state space representation of a certain canonical form? If yes, which one? (5 
pts) 
(In the sub-question a, you do not have to submit the A matrix to collect points, but having 
the A matrix can still help you to give a correct answer to the sub-question b)

### Page 5

You can answer in Dutch as well 
5 
 
Controller analysis and design - 1) (60 pts, 75 mins)  
 
Consider an inverted pendulum of length L and mass m on a moving cart of mass, M. It is assumed 
that the cart moves on a frictionless, flat plane. The force 𝑓(𝑡), applied to the cart is the input, while 
the first output is the angular deflection, 𝜃(𝑡), of the pendulum from the vertical. The second output 
is the displacement of the cart from a fixed point is given by q(𝑡). A linear state-space representation 
of the plant is given by  
𝒙̇ = [
0
0
1
0
0
0
0
1
10.78
0
0
0
−0.98
0
0
0
] 𝒙+ [
0
0
−1
1
] 𝑢 
𝒚= [1
0
0
0
0
1
0
0] 𝒙+ [0
0] 𝑢
 
The state-vector of this fourth order plant is 𝒙(𝑡) = [𝜃(𝑡); 𝑞(𝑡); 𝜃̇(𝑡); 𝑞̇(𝑡)]
𝑇 with the SI-units  
𝜃 in 𝑟𝑎𝑑,  
𝑞 in 𝑚,  
𝜃̇ in 𝑟𝑎𝑑/𝑠, and  
𝑞̇ in 𝑚/𝑠

### Page 6

You can answer in Dutch as well 
6 
 
a) The control law is given as 
 𝑢(𝑡) = 1362.36 𝜃(𝑡) + 909.31 𝑞(𝑡) + 344.87 𝜃̇(𝑡) + 313.46 𝑞̇(𝑡) because all states are 
measurable. Determine the closed-loop pole locations for the given control strategy. (8 pts) 
--------------------------------------------------------------------------------------------------------------------------- 
 
 
b) It is desired to move the cart by 1 𝑚, while not letting the pendulum fall. 
Such an inverted pendulum represents a drink being brought to you by a 
robot (approximated by the moving cart). Update the control law given in 
a) to make the reference tracking possible. Write the new control law as 
an equation starting with 𝑢(𝑡) = ⋯  (7 pts) 
 
(Important remark: You are not allowed to change the closed-loop pole 
locations.) 
-------------------------------------------------------------------------------------------------------------------------------- 
 
c) Show and discuss, using the necessary graphs and the Matlab implementation, whether the 
robot can reach the reference position of 𝑟= 1𝑚 without dropping your drink in a 
reasonable time. The drink is dropped if the robot is tilted too much (𝑙𝑎𝑟𝑔𝑒 𝜃). Explain your 
interpretation of the results and avoid answering by just copy-pasting your code. (15 pts) 
 
-it must be assumed that the mass of the drink is negligible and there is no saturation 
on the input (actuation) side. 
-if you make any other assumptions, mention them. 
-indicate the code that generates the graph you want to show if you need to show 
something on the graph. 
-1 𝑟𝑎𝑑 = 57.29° 
-for this sub-question, the closed-loop pole locations that you determined in a) 
cannot be changed freely. 
-------------------------------------------------------------------------------------------------------------------------------- 
 
 
d) Your friend calls you in panic and tells you that one of the sensors is broken and that he can 
get only one of the two outputs. He does not know which sensor is broken and calls you over 
to fix the controller. You calm your friend down by telling him that you can update the 
algorithm such that the pendulum on a moving cart system can be stabilized using the only 
sensor that is still working. After hanging up the phone, you realize that you might have 
talked big (or overconfident) stating that you can fix the algorithm to work with just one 
sensor. 
 
Which sensor do you wish to have it still functioning? 𝜃(𝑡) or 𝑞(𝑡) and why? Show your 
calculations/reasoning. (6 pts) 
--------------------------------------------------------------------------------------------------------------------------------

### Page 7

You can answer in Dutch as well 
7 
 
 
e) Assume that the sensor you wished was functioning, is still functioning. Explain how you can 
fix the robot’s control algorithm to use only one sensor measurement using Matlab. If your 
conclusion in c) was that the robot’s performance was poor, you can now update the 
algorithm into a better one. (24 pts) 
-Your answer should at least contain 1) the control law and 2) the following graph: 
Response graph of the compensator-based tracking system for inverted-pendulum on 
a moving cart, with desired angular position 𝜃𝑑(𝑡) = 0, and desired cart’s 
displacement, 𝑞𝑑(𝑡) = 1𝑚, in which a comparison between the real states and the 
estimated states is visible. 
Hints:  
1) Use the plant initial conditions 𝑞0 = [0.1          0     −0.1       0.03]. Observer initial conditions 
should be [0       0         0        0] 
2)  The observer poles can be placed on 
 [-20+20*i -20-20*i -10+10*i -10-10*i] 
 
 
From now on, the given control law in a) and the desired closed-loop pole locations, 
can be changed freely to an alternative of your choosing.

