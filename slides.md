# OBS7 Lecture Slides

## Slide 1

Observers for State Space Systems

1

## Slide 2

Observers for State Space Systems

2

## Slide 3

Observers for State Space Systems

3

## Slide 4

Observers for State Space Systems OBS7Lecture 1-2: Introduction to State Space,Stability, Hurwitz, Eigenvalues, Eigenvectors

## Slide 5

Observers for State Space Systems

5

## Slide 6

Observers for State Space Systems

6

## Slide 7

Observers for State Space Systems

7

## Slide 8

Observers for State Space Systems

8

Information about the teacher

Name:		Albert Aslan
E-mail:		a.aslan@fontys.nl
Room:		R1_0.173
Tel:		06 232 946 37

## Slide 9

Observers for State Space Systems

9

Overall information 1

Course name:		OBS7 
				Observers for State Space Systems
Scope:			4 ECTS
Materials:		-Handouts Powerpoint
				-Mandatory: "Feedback Control of 				Dynamic Systems, Global Edition" 				from Gene F. Franklin e.a. (7th edition),  			ISBN13: 9781292068909

## Slide 10

Observers for State Space Systems

10

Overall information 2

Lectures: 		2x2 hours for 6 weeks
Exam:			Digital exam for 100 min. 					About the whole course
Practicals:		2 sessions (except week 3,5 or week 4,6) 			as half class (attendance mandatory for 			the ones with Quanser setups)
				Must be graded satisfactory for the full 			allocation of the course credits
Allowed in exam:	Open book (not your own notes)
				A calculator, MATLAB/Simulink and 			your own computer, 
	Any means of online communication will result in disciplinary actions.

## Slide 11

Planning

11

## Slide 12

What is an observer?
Why do we need an observer?


Let’s watch a video
https://nl.mathworks.com/videos/understanding-kalman-filters-part-1-why-use-kalman-filters--1485813028675.html

Observers for State Space Systems

12

Introduction

## Slide 13

The state equation and the output equation of a linear system can be written as matrices:

Observers for State Space Systems

13

STATE SPACE SYSTEMS

## Slide 14

Observers for State Space Systems

14

Matrix recap

## Slide 15

Observers for State Space Systems

15

Matrix recap

## Slide 16

Observers for State Space Systems

16

Matrix recap

## Slide 17

Observers for State Space Systems

17

Matrix recap - Product

## Slide 18

Observers for State Space Systems

18

Matrix recap - Transpose

## Slide 19

Observers for State Space Systems

19

Matrix recap - Determinant

## Slide 20

Observers for State Space Systems

20

Matrix recap - Determinant

## Slide 21

Observers for State Space Systems

21

Matrix recap - Determinant

## Slide 22

The rank of a matrix is the number of its linearly independent rows or columns.

Observers for State Space Systems

22

Matrix recap - Rank

## Slide 23

The rank of a matrix is the number of its linearly independent rows or columns.

Observers for State Space Systems

23

Matrix recap - Rank

## Slide 24

Observers for State Space Systems

24

Matrix recap – Characteristic Polynomial

## Slide 25

Observers for State Space Systems

25

Matrix recap – Eigenvalues & Eigenvectors

## Slide 26

Observers for State Space Systems

26

Matrix recap – Eigenvalues & Eigenvectors

## Slide 27

Observers for State Space Systems

27

Matrix recap – Eigenvalues & Eigenvectors

## Slide 28

Observers for State Space Systems

28

Matrix recap – Eigenvalues & Eigenvectors

## Slide 29

Observers for State Space Systems

29

Matrix recap – Eigenvalues & Eigenvectors

## Slide 30

Observers for State Space Systems

30

Matrix recap – Eigenvalues & Eigenvectors

## Slide 31

Observers for State Space Systems

31

Stability in State Space

## Slide 32

Write a Matlab function isStable(A,B,C,D)
that returns the boolean value (true or false) if the system is stable.

Observers for State Space Systems

32

Assignment

## Slide 33

function [ boolean ] = isStable( A,B,C,D)
 
	E = eig(A);
 
	positive_eigenvalues = E(E>0);
 
	if any(positive_eigenvalues) == 1
    
    		boolean = 0;
    
	else 
    
    		boolean = 1;

	end
end

Observers for State Space Systems

33

Assignment

## Slide 34

Observers for State Space Systems

34

Deriving the state space model

What is the input and output?
What are the differential equations
What is the order?
Which state vector should be defined?

Next, express the differential equation using only state variables and input/output variables.

## Slide 35

Observers for State Space Systems

35

Deriving the state space model

Next, express the differential equation using only state variables and input/output variables.

Always answer the following questions first:

## Slide 36

Observers for State Space Systems

36

## Slide 37

How to formulate state space systems?

37

## Slide 38

How to formulate state space systems?

38

## Slide 39

How to formulate state space systems?

39

## Slide 40

How to formulate state space systems?

40

## Slide 41

How to formulate state space systems?

41

## Slide 42

How to formulate state space systems?

42

## Slide 43

How to formulate state space systems?

43

## Slide 44

How to formulate state space systems?

44

## Slide 45

How to formulate state space systems?

45

## Slide 46

Observers for State Space Systems

46

## Slide 47

How to formulate TF from SS?

47

## Slide 48

How to formulate TF from SS?

48

## Slide 49

How to formulate TF from SS?

49

## Slide 50

How to formulate TF from SS?

50

## Slide 51

Find the state space representation of the following two cart system with friction on the wheels.

Observers for State Space Systems

51

Homework

## Slide 52

Homework

Observers for State Space Systems

52

## Slide 53

http://lpsa.swarthmore.edu/MtrxVibe/EigMat/MatrixEigen.html
https://nl.mathworks.com/matlabcentral/answers/136427-pid-gains-from-a-transfer-function-of-a-mass-spring-damper-system
Feedback Control of Dynamic Systems, 7th edition, Franklin et. al. Global Edition. Pearson.
http://www.mathsisfun.com/algebra/matrix-determinant.html
https://en.wikipedia.org/wiki/Hurwitz_matrix

Observers for State Space Systems

53

List of resources

## Slide 54

OBS7Observers for State Space SystemsLecture 3: State Feedback Control and Pole Placement

## Slide 55

Planning

55

## Slide 56

Observers for State Space Systems

56

Homework (Solutions)

## Slide 57

Homework (Solutions)

Observers for State Space Systems

57

## Slide 58

Homework (Solutions)

Observers for State Space Systems

58

## Slide 59

Homework (Solutions)

Observers for State Space Systems

59

## Slide 60

Full-state feedback

The purpose: Assign a set of pole locations 
(aim for good rise-time, settling-time, overshoot, and steady state error)



Assumption: we have access to all the states (i.e. accelerometer, tachometer, position encoder are all available)

Observers for State Space Systems

60

## Slide 61

Recap- root locus (limited freedom of pole locations)

Observers for State Space Systems

61

## Slide 62

Full-state Feedback Control (chapter 7.5)

62

Compare this block diagram with output feedback. Which one can perform better?

Output feedback

State feedback

## Slide 63

Full-state Feedback Control (chapter 7.5)

63

Compare this block diagram withoutput feedback. Which one can perform better?

Output feedback

State feedback

## Slide 64

Full-state Feedback Control (chapter 7.5)

64

Each state has its own K, more effect on the poles, more freedom

## Slide 65

Full-state Feedback Control (chapter 7.5)

65

Each state has its own K, more effect on the poles, more freedom

Note that: reference = 0

## Slide 66

Explanation: full-state feedback vs. reality

“We assume for feedback purposes that all the elements of the state vector are at our disposal which is why we refer to this as “full-state,” feedback. In practice, of course, this would usually be a ridiculous assumption; moreover, a well-trained control designer knows that other design methods do not require so many sensors. The assumption that all state-variables are available merely allows us to proceed with this first step.”

Observers for State Space Systems

66

## Slide 67

Analysis of full-state feedback

Observers for State Space Systems

67

## Slide 68

Analysis of full-state feedback

Observers for State Space Systems

68

## Slide 69

Analysis of full-state feedback

Observers for State Space Systems

69

## Slide 70

Analysis of full-state feedback

Observers for State Space Systems

70

## Slide 71

Example: Full state feedback

Observers for State Space Systems

71

## Slide 72

Example: Full state feedback

Observers for State Space Systems

72

## Slide 73

Example: Full state feedback

Since the system is stable, all the states and output returns to 0 after some time. (because ref=0)

Let’s place the poles to    -4, -5, and -6 for faster reaction, K=?

Observers for State Space Systems

73

## Slide 74

Example: Full state feedback

Observers for State Space Systems

74

## Slide 75

Example: Full state feedback

Observers for State Space Systems

75

## Slide 76

Example: Full state feedback

Observers for State Space Systems

76

Before state fb

Before state fb

After state feedback

After state feedback

## Slide 77

Example: Full state feedback

Observers for State Space Systems

77

## Slide 78

“Selecting desirable root locations is an inexact science that may require some iteration by the designer.”

Observers for State Space Systems

78

## Slide 79

Assignment (Example 7.14, given the pole locations)

Observers for State Space Systems

79

## Slide 80

Assignment solutions

Observers for State Space Systems

80

## Slide 81

Matlab code to simulate state space responses

A=[0 1;-1 0];  B=[0;1];
C=[1 0];       K=[3 4];
Acl=A-B*K;
t=0:0.1:7;
sysCL = ss(Acl,[0;0],[C;0 1;-K/4],0);
y2 = lsim(sysCL,zeros(length(t),1)',t,[1;0]);
figure; plot(t,y2,'LineWidth',2)


xlabel('Time (sec)');
ylabel('Amplitude');
text(1.7,-.3,'x_2');
text(.5,.1,'u/4'); 
text(.7,.7,'x_1');
title('Free response of the oscillator with full state feedback');
grid;

Observers for State Space Systems

81

## Slide 82

Ackermann’s Formula, Pole Placement

Observers for State Space Systems

82

## Slide 83

Ackermann’s Formula, Pole Placement

Observers for State Space Systems

83

## Slide 84

Ackermann’s Formula, Pole Placement

Observers for State Space Systems

84

## Slide 85

Ackermann’s Formula: The main algorithm

Observers for State Space Systems

85

## Slide 86

Ackermann’s Formula: Example

Observers for State Space Systems

86

## Slide 87

Ackermann’s Formula: Example (Solutions)

Observers for State Space Systems

87

## Slide 88

Ackermann’s Formula: Example (Solutions)

Observers for State Space Systems

88

## Slide 89

Ackermann’s Formula: Example (Solutions)

Observers for State Space Systems

89

## Slide 90

Ackermann’s Formula: Example (Solutions)

Observers for State Space Systems

90

## Slide 91

Ackermann’s Formula: Example (Solutions)

Observers for State Space Systems

91

## Slide 92

Ackermann’s Formula: in MATLAB

Observers for State Space Systems

92

In MATLAB the three steps of Ackermann’s formula can be implemented easily.

>> wo = 1;
>> A = [ 0 1; -wo*wo 0];
>> B = [0;1];
>> desired_poles = [-2*wo;-2*wo];
>> K = acker(A,B,desired_poles)

K =

     3     4

## Slide 93

Ackermann’s Formula: in MATLAB

Observers for State Space Systems

93

## Slide 94

Controllability

Observers for State Space Systems

94

In rare instances the system may be uncontrollable, in which case no possible control will yield arbitrary pole locations. Uncontrollable systems have certain modes, or subsystems, that are unaffected by the control.

Parts of the system are physically disconnected

## Slide 95

Controllability

Observers for State Space Systems

95

## Slide 96

Controllability – state space

How do we recognize it from numbers and matrices?
Consider the following numerical example


This system has two roots (3 and -2) and hence unstable due to positive pole at 3.

The control effort exists only for the unstable mode (+3), that’s why the system is uncontrollable (but stabilizable).

Uncontrollable = you can’t place all the poles to wherever you want

Observers for State Space Systems

96

## Slide 97

Controllability matrix

Observers for State Space Systems

97

## Slide 98

Controllability – Example

Observers for State Space Systems

98

## Slide 99

Controllability – Example (solution)

Observers for State Space Systems

99

## Slide 100

Controllability – Example (solution)

Observers for State Space Systems

100

## Slide 101

Observers for State Space Systems

101

Controllable

Almost uncontrollable

Uncontrollable 
(extra actuation needed, like abs)

## Slide 102

Summary Pole Placement

Observers for State Space Systems

102

## Slide 103

Assigment

Observers for State Space Systems

103

## Slide 104

Homework

Observers for State Space Systems

104

## Slide 105

OBS7Observers for State Space SystemsLecture 4: Reference Input with Full-State Feedback

## Slide 106

Planning

106

## Slide 107

Homework (Solutions)

Observers for State Space Systems

107

## Slide 108

Homework (Solutions)

Observers for State Space Systems

108

## Slide 109

Homework (Solutions)

Observers for State Space Systems

109

## Slide 110

So far we have looked at how to pick K to get the dynamics to have some nice properties (i.e. stabilize A) 

The question remains as to how well this controller allows us to track a reference command? 
	Performance issue rather than just stability.

Observers for State Space Systems

110

10/lecture-notes/MIT16_30F10_lec11.pdf

## Slide 111

Basic pole placement

Observers for State Space Systems

111

## Slide 112

Introducing the Reference Input

Observers for State Space Systems

112

## Slide 113

Observers for State Space Systems

113

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

## Slide 114

Observers for State Space Systems

114

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

## Slide 115

Observers for State Space Systems

115

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

## Slide 116

Observers for State Space Systems

116

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

## Slide 117

Observers for State Space Systems

117

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

## Slide 118

Observers for State Space Systems

118

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

## Slide 119

Observers for State Space Systems

119

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

## Slide 120

Observers for State Space Systems

120

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

## Slide 121

Observers for State Space Systems

121

## Slide 122

Example

Observers for State Space Systems

122

## Slide 123

Solution

Observers for State Space Systems

123

## Slide 124

Solution

Observers for State Space Systems

124

## Slide 125

Solution

Observers for State Space Systems

125

## Slide 126

Solution

Observers for State Space Systems

126

## Slide 127

Alternative Approach – Reference Tracking

Observers for State Space Systems

127

## Slide 128

Alternative Approach – Reference Tracking

Observers for State Space Systems

128

Note that here “1” is used in
place of the identity matrix which
is used in the derivation. This 
is because we are focused on
SISO systems.

## Slide 129

Alternative Approach – Reference Tracking

Observers for State Space Systems

129

## Slide 130

Homework

Observers for State Space Systems

130

## Slide 131

OBS7Observers for State Space SystemsLecture 5-6: Controllability, Observability, and Cannonical Forms

## Slide 132

Planning

132

## Slide 133

Homework (Solutions)

Observers for State Space Systems

133

## Slide 134

Homework (Solutions)

Observers for State Space Systems

134

## Slide 135

Homework (Solutions)

Observers for State Space Systems

135

## Slide 136

Observability

Observers for State Space Systems

136

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

## Slide 137

Observability

Observers for State Space Systems

137

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

## Slide 138

Observability

Observers for State Space Systems

138

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

## Slide 139

Observability

Observers for State Space Systems

139

99 extra states?

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

## Slide 140

Observability

Observers for State Space Systems

140

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

## Slide 141

Observability

Observers for State Space Systems

141

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

## Slide 142

Observability

Observers for State Space Systems

142

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

## Slide 143

Observability

Observers for State Space Systems

143

## Slide 144

Example Unobservable System

Cruise control in the bus does not measure the internal temperature of the engine, although it plays a role in the transfer function from throttle to speed.

Observers for State Space Systems

144

## Slide 145

Controllability

Observers for State Space Systems

145

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

## Slide 146

Controllability

Observers for State Space Systems

146

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

## Slide 147

Controllability/Observability

Observers for State Space Systems

147

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

## Slide 148

Controllability/Observability

Observers for State Space Systems

148

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

## Slide 149

Controllability/Observability

Observers for State Space Systems

149

Controllability Matrix

ObservabilityMatrix

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

## Slide 150

Controllability/Observability - Example

Observers for State Space Systems

150

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

## Slide 151

Controllability/Observability - Assignment

Observers for State Space Systems

151

Find the controllability and observability matrices and draw conclusions about the controllability and observability of this system (without MATLAB).

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

## Slide 152

Canonical Forms in State Space

There are three canonical forms (ways of representation) in state space systems.
Control canonical form
Modal canonical form
Observer canonical form

Observers for State Space Systems

152

## Slide 153

Control Canonical Form

Observers for State Space Systems

153

## Slide 154

Control Canonical Form

Observers for State Space Systems

154

## Slide 155

Control Canonical Form

Observers for State Space Systems

155

Possible to build SS by inspection

Output of the integrator = state
Input of the integrator = state derivative

## Slide 156

Control Canonical Form

Observers for State Space Systems

156

## Slide 157

Modal Canonical Form

Observers for State Space Systems

157

## Slide 158

Modal Canonical Form

Call the integrator outputs the states,
Call the integrator inputs the state derivatives

Observers for State Space Systems

158

## Slide 159

Modal Canonical Form

Observers for State Space Systems

159

## Slide 160

Modal Canonical Form

Observers for State Space Systems

160

Difficulties with modal canonical form:
Complex poles -> A matrix elements being complex
Repeated poles -> no diagonal A matrix

## Slide 161

Modal Canonical Form

Example 2: The quarter car model

Observers for State Space Systems

161

## Slide 162

Modal Canonical Form

Observers for State Space Systems

162

## Slide 163

Modal Canonical Form

Observers for State Space Systems

163

## Slide 164

Modal Canonical Form

Observers for State Space Systems

164

Control canonical form

## Slide 165

Modal Canonical Form

Observers for State Space Systems

165

In Matlab

## Slide 166

Observer Canonical Form

Observers for State Space Systems

166

## Slide 167

Observer Canonical Form

Observers for State Space Systems

167

## Slide 168

Observer Canonical Form

Observers for State Space Systems

168

Control Canonical Form            vs.         Observer Canonical Form

## Slide 169

Observer Canonical Form

Observers for State Space Systems

169

Possible to build SS by inspection

Output of the integrator = state
Input of the integrator = state derivative

## Slide 170

Observer Canonical Form

Observers for State Space Systems

170

## Slide 171

Transformations

Observers for State Space Systems

171

## Slide 172

Transformations

Observers for State Space Systems

172

## Slide 173

Transformations – in Matlab

Observers for State Space Systems

173

## Slide 174

Transformations – in Matlab

Observers for State Space Systems

174

## Slide 175

Homework

Observers for State Space Systems

175

## Slide 176

Homework

Observers for State Space Systems

176

## Slide 177

OBS7Observers for State Space SystemsLecture 7-8: Luenberger Observer and Stability of the Observer

## Slide 178

Planning

178

## Slide 179

Homework (Solutions)

Observers for State Space Systems

179

## Slide 180

Homework (Solutions)

Observers for State Space Systems

180

## Slide 181

Homework (Solutions)

Observers for State Space Systems

181

## Slide 182

Homework (Solutions)

Observers for State Space Systems

182

## Slide 183

Homework (Solutions)

Observers for State Space Systems

183

## Slide 184

Homework (Solutions)

Observers for State Space Systems

184

## Slide 185

Homework (Solutions)

Observers for State Space Systems

185

## Slide 186

Estimators/Observers

Observers for State Space Systems

186

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

## Slide 187

Estimators/Observers

Observers for State Space Systems

187

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

## Slide 188

Estimation  Schemes

Observers for State Space Systems

188

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

## Slide 189

Observers for State Space Systems

189

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

## Slide 190

Open-loop Estimator

Observers for State Space Systems

190

All the muscle contractions, pace length

Eye measurements

## Slide 191

Open-loop  Estimator

Observers for State Space Systems

191

Actual System
x:  A, B, C

Estimator
xˆ:  A, B, C

y

yˆ

u

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

## Slide 192

Open-loop Estimator

Observers for State Space Systems

192

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

## Slide 193

Open-loop Estimator

Observers for State Space Systems

193

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

## Slide 194

Open-loop Estimator

Observers for State Space Systems

194

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

## Slide 195

Closed-loop Estimator

Observers for State Space Systems

195

Actual System
x:  A, B, C

Estimator
xˆ:  A, B, C

L

y˜

u

yˆ

−

y

+

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

## Slide 196

Closed-loop Estimator

Observers for State Space Systems

196

All the muscle contractions, pace length

Eye measurements

But now assume that we know what the output must have been.

## Slide 197

Closed-loop Estimator

Assume that the path is wider.
You get to hear constantly what the output (positioning in the corridor) must have been.

Observers for State Space Systems

197

## Slide 198

Closed-loop Estimator

Observers for State Space Systems

198

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

## Slide 199

Closed-loop Estimator

Observers for State Space Systems

199

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

## Slide 200

Closed-loop Estimator

Observers for State Space Systems

200

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

## Slide 201

Observers for State Space Systems

201

## Slide 202

Example

Observers for State Space Systems

202

## Slide 203

Example

Building the first observer in Simulink (Observer_simple_2nd_order.mdl)

Observers for State Space Systems

203

## Slide 204

Example

Inside the Estimator Subsystem (Observer_simple_2nd_order>Esimator)

Observers for State Space Systems

204

## Slide 205

205

## Slide 206

Observers for State Space Systems

206

## Slide 207

Regulator/Estimator Comparison

Observers for State Space Systems

207

They are called dual problems.

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

## Slide 208

Estimation Gain Selection

Observers for State Space Systems

208

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

## Slide 209

Estimation Gain Selection

Observers for State Space Systems

209

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

## Slide 210

Recap Ackermann’s Formula: The main algorithm

Observers for State Space Systems

210

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

## Slide 211

Observers for State Space Systems

211

Note that all these analyses are possible with control/observer canonical forms!

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

## Slide 212

Esimators Example

Observers for State Space Systems

212

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

## Slide 213

Observers for State Space Systems

213

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

## Slide 214

Observers for State Space Systems

214

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

## Slide 215

Observers for State Space Systems

215

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

## Slide 216

Open-loop estimator error converges to zero, but very slowly.

Observers for State Space Systems

216

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

## Slide 217

Closed-loop estimator. Convergence looks much better.

Observers for State Space Systems

217

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

## Slide 218

Where to Put Estimator Poles?

Observers for State Space Systems

218

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

## Slide 219

Where to Put Estimator Poles?

Observers for State Space Systems

219

Diﬀerent concerns for the estimator:
Loop closed inside computer, so saturation not a problem.
However, measurements y are often “noisy”, and must be careful how we use them to develop state estimates.

⇒ High bandwidth estimators tend to accentuate the eﬀect of sensing noise in the estimate.
State  estimates  tend  to  “track”  the  data  in  the  measurements, which could be ﬂuctuating randomly due to the noise.

⇒ Low bandwidth estimators have lower gains and tend to rely more heavily on the plant model
Essentially an open­-loop estimator – tends to ignore the measurements and just uses the plant model.

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

## Slide 220

Example – High Bandwidth Estimator

Observers for State Space Systems

220

## Slide 221

Example – High Bandwidth Estimator

w0=3
A=[0 1;-w0^2 0];
B=[0;1];
C=[1 0];
D = 0;
L_low_bw = [2*w0; 9*w0^2];

desired_poles = 15*eig(A-B*K);
L_transpose = acker(A',C',desired_poles) ;
L2=L_transpose'; %high_bandwidth L

Observers for State Space Systems

221

## Slide 222

Low bandwidth observer

Observers for State Space Systems

222

## Slide 223

High Bandwidth Observer

Observers for State Space Systems

223

## Slide 224

Normal Bandwidth Observer

Observers for State Space Systems

224

## Slide 225

What Happens with Output Noise

Observers can be used to observe the correct states/outputs when noise is present.

Observers for State Space Systems

225

## Slide 226

Normal Bandwidth Observer with Output Noise

Observers for State Space Systems

226

## Slide 227

High Bandwidth Observer with Output Noise

Observers for State Space Systems

227

## Slide 228

Final Thoughts

228

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

Observers for State Space Systems

## Slide 229

Final Thoughts

229

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

Observers for State Space Systems

## Slide 230

Code: Estimator

% Examples of estimator performance
%
% Jonathan How  Oct 2010   plant dynamics
%
close all;clear all
set(0,'DefaultLineLineWidth',2);
set(0,'DefaultlineMarkerSize',10);set(0,'DefaultlineMarkerFace','b')
set(0, 'DefaultAxesFontSize', 12);set(0, 'DefaultTextFontSize', 12)
 
set(0,'DefaultFigureColor','w',...
    'DefaultAxesColor','w',...
    'DefaultAxesXColor','k',...
    'DefaultAxesYColor','k',...
    'DefaultAxesZColor','k',... 
    'DefaultTextColor','k')
    
a=[-1 1.5;1 -2];b=[1 0]';c=[1 0];d=0;
%
% estimator gain calc 
l=place(a',c',[-3 -4]);l=l'
%
% plant initial cond 
xo=[-.5;-1];
% extimator initial cond 
xe=[0 0]';
% 
t=[0:.1:10];
% inputs 
u=0;u=[ones(15,1);-ones(15,1);ones(15,1)/2;-ones(15,1)/2;zeros(41,1)];

230

% inputs 
u=0;u=[ones(15,1);-ones(15,1);ones(15,1)/2;-ones(15,1)/2;zeros(41,1)];
%
% open?loop estimator
A_ol=[a zeros(size(a));zeros(size(a)) a]; B_ol=[b;b];
C_ol=[c zeros(size(c));zeros(size(c)) c]; D_ol=zeros(2,1);
%
% closed?loop estimator
A_cl=[a zeros(size(a));l*c a-l*c]; B_cl=[b;b];
C_cl=[c zeros(size(c));zeros(size(c)) c]; D_cl=zeros(2,1);
 
[y_cl,x_cl]=lsim(A_cl,B_cl,C_cl,D_cl,u,t,[xo;xe]);
[y_ol,x_ol]=lsim(A_ol,B_ol,C_ol,D_ol,u,t,[xo;xe]);
 
figure(1);clf;subplot(211) 
set(gca)
plot(t,x_cl(:,[1 2]),t,x_cl(:,[3 4]),'--','LineWidth',2);
axis([0 4 -1 1]); title('Closed?loop estimator');ylabel('states');xlabel('time') 
text(.25,-.4,'x 1');text(.5,-.55,'x 2');subplot(212)
plot(t,x_cl(:,[1 2])-x_cl(:,[3 4]))
axis([0 4 -1 1]);grid on 
ylabel('estimation error');xlabel('time')
 
figure(2);clf;subplot(211) 
set(gca)
plot(t,x_ol(:,[1 2]),t,x_ol(:,[3 4]),'--','LineWidth',2);axis([0 4 -1 1])
title('Open loop estimator');ylabel('states');xlabel('time') 
text(.25,-.4,'x 1');text(.5,-.55,'x 2');subplot(212)
plot(t,x_ol(:,[1 2])-x_ol(:,[3 4]))
axis([0 4 -1 1]);grid on 
ylabel('estimation error');xlabel('time')

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

Observers for State Space Systems

## Slide 231

Homework

Observers for State Space Systems

231

## Slide 232

Homework

Observers for State Space Systems

232

## Slide 233

OBS7Observers for State Space SystemsLecture 9: State Feedback Control Using the Observed States

## Slide 234

Planning

234

## Slide 235

Homework (Solutions)

Observers for State Space Systems

235

## Slide 236

Homework (Solutions)

Observers for State Space Systems

236

## Slide 237

Homework (Solutions)

Observers for State Space Systems

237

## Slide 238

Homework (Solutions)

Observers for State Space Systems

238

## Slide 239

Homework (Solutions)

Observers for State Space Systems

239

## Slide 240

Homework (Solutions)

Observers for State Space Systems

240

## Slide 241

Combined Estimators and Regulators

Observers for State Space Systems

241

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

## Slide 242

Combined Estimators and Regulators

Observers for State Space Systems

242

Note that these are vectors

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

## Slide 243

Combined Estimators and Regulators

Observers for State Space Systems

243

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

## Slide 244

Combined Estimators and Regulators

Observers for State Space Systems

244

If this is stable, state-feedback works fine.

If this is stable, observer works fine.

## Slide 245

Combined Estimators and Regulators

245

1

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

## Slide 246

Combined Estimators and Regulators

Observers for State Space Systems

246

If this is stable, state-feedback works fine.

If this is stable, observer works fine.

2

1&2

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

## Slide 247

Combined Estimators and Regulators

Observers for State Space Systems

247

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

## Slide 248

Combined Estimators and Regulators

So we can just design the estimator/regulator separately and combine them at the end.
Called the Separation Principle
Keep in mind that the pole locations you are picking for these two sub-problems will also be the closed-loop pole locations.


Note: Separation principle means that there will be no ambiguity or uncertainty about the stability and/or performance of the closed-loop system.
The closed-loop poles will be exactly where you put them!!

Observers for State Space Systems

248

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

## Slide 249

The Compensator

To compare the state-variable method of design with CEN4B/ACE7 type of design (classical controllers), we note that the blue shaded portion corresponds to a compensator.

Observers for State Space Systems

249

y

r

e

u

Gp(s)

Dc(s)

-

We can even implement this (dynamic) compensator with reference input later on to compare.

## Slide 250

The Compensator

Observers for State Space Systems

250

## Slide 251

The Compensator

Observers for State Space Systems

251

## Slide 252

The Unstable Compensator Example

Observers for State Space Systems

252

## Slide 253

The Unstable Compensator Example

Connect these systems as given below using feedback(sys1,sys2)

Observers for State Space Systems

253

## Slide 254

The Unstable Compensator Example

Observers for State Space Systems

254

>>sys_CL = feedback(sys,sys_c)

## Slide 255

The Unstable Compensator Example

So we have an unstable compensator that yields a stable closed loop.


>>impulse(sys_cl)			>>impulse(sys_c)

Observers for State Space Systems

255

## Slide 256

The Unstable Compensator Example

Observers for State Space Systems

256

## Slide 257

The Unstable Compensator Example

Compensator Bode

Observers for State Space Systems

257

“An unstable compensator is typically not acceptable because of the difficulty in testing either the compensator by itself or the system in open loop during a bench checkout. 

In some cases, however, better control can be achieved with an unstable compensator; then its inconvenience in checkout may be worthwhile.

There are even systems that cannot be stabilized with a stable compensator.”

## Slide 258

The Compensator

Observers for State Space Systems

258

Reference: Jonathan How, and Emilio Frazzoli. 16.30 Feedback Control Systems. Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

## Slide 259

Homework

Observers for State Space Systems

259

## Slide 260

Homework

Observers for State Space Systems

260

## Slide 261

Homework

Observers for State Space Systems

261

## Slide 262

Homework

Observers for State Space Systems

262

## Slide 263

OBS7Observers for State Space SystemsLecture 10: Introduction of the Reference Input with the Estimator

## Slide 264

Planning

264

## Slide 265

Homework (Solutions)

Observers for State Space Systems

265

## Slide 266

Homework (Solutions)

Observers for State Space Systems

266

## Slide 267

Homework (Solutions)

Observers for State Space Systems

267

## Slide 268

Homework (Solutions)

Observers for State Space Systems

268

## Slide 269

Homework (Solutions)

Observers for State Space Systems

269

## Slide 270

Homework (Solutions)

Observers for State Space Systems

270

## Slide 271

Homework (Solutions)

Observers for State Space Systems

271

## Slide 272

Homework (Solutions)

Observers for State Space Systems

272

## Slide 273

Homework (Solutions)

Observers for State Space Systems

273

## Slide 274

Homework (Solutions)

Observers for State Space Systems

274

## Slide 275

Homework (Solutions)

Observers for State Space Systems

275

## Slide 276

Homework (Solutions)

Observers for State Space Systems

276

## Slide 277

Homework (Solutions)

Observers for State Space Systems

277

## Slide 278

Homework (Solutions)

Observers for State Space Systems

278

## Slide 279

Reference Input

The controller obtained by combining the control law with estimator is a regulator design.
This means that the characteristic equations of the control and the estimator are chosen for good disturbance rejection.

Observers for State Space Systems

279

## Slide 280

What is Disturbance Rejection

Observers for State Space Systems

280

Regulator keeps it at zero position

## Slide 281

Reference Input

Observers for State Space Systems

281

## Slide 282

Reference Input

Observers for State Space Systems

282

## Slide 283

Reference Input – Type 1: Autonomous Estimator

Observers for State Space Systems

283

## Slide 284

Reference Input – Type 1: Autonomous Estimator

Observers for State Space Systems

284

## Slide 285

Reference Input – Type 1: Autonomous Estimator

Observers for State Space Systems

285

## Slide 286

Example – Type 1: Autonomous Estimator

Compensator_2nd_order_reference_tracking.mdl

Compensator:






			Overall diagram:

Observers for State Space Systems

286

## Slide 287

Example – Type 1

Observers for State Space Systems

287

## Slide 288

Reference Input – Type 2: Tracking-error Estimator

This solution is sometimes forced on the control designer when the sensor measures only the output error.
Example: In thermostats the output is the difference between outside and reference temperature.

Observers for State Space Systems

288

## Slide 289

Reference Input – Type 2: Tracking-error Estimator

Observers for State Space Systems

289

## Slide 290

Reference Input – Type 2: Tracking-error Estimator

Observers for State Space Systems

290

## Slide 291

Reference Input – Type 2: Tracking-error Estimator

Observers for State Space Systems

291

## Slide 292

Reference Input – Type 2: Tracking-error Estimator

Observers for State Space Systems

292

## Slide 293

Reference Input – Type 2: Tracking-error Estimator

Observers for State Space Systems

293

## Slide 294

Reference Input – Type 2: Tracking-error Estimator

Observers for State Space Systems

294

## Slide 295

Example – Type 2: Tracking-error Estimator

Lets simulate the inverted pendulum system in Simulink.

w0=3
A=[0 1;-w0^2 0]; B=[0;1];
C=[1 0]; D = 0;

K=[3*w0^2 4*w0];
Acl = [A -B*K;L*C A-B*K-L*C];
Nbar = inv(-[C 0 0]*inv(Acl)*[0;0;-L]);

desired_poles = 2*eig(A-B*K);
L = acker(A',C',desired_poles)' ; %normal_bandwidth L

Observers for State Space Systems

295

## Slide 296

Example – Type 2: Tracking-error Estimator

The estimation is not succesful, but reference tracking is.

How, why?

Can we solve that?

Disadvantage of Type 2: High overshoot because of the zero of the compensator.

Observers for State Space Systems

296

## Slide 297

Homework

Search a model in the book (transfer function or state-space) that is interesting for you
Implement the Autonomous Estimator using Simulink, which includes
Only the output measurement is available
State estimation
Full-state feedback using estimated states
Reference tracking


No answers will be supplied for this homework but it is very useful for the exam.

Observers for State Space Systems

297

## Slide 298

OBS7Observers for State Space SystemsLecture 11: Disturbance (augmented) Observers

## Slide 299

Planning

299

## Slide 300

Augmenting the State Space Equations

A special topic in state space design.

Aim is to learn the tricks with augmenting (making the matrices bigger) the state space equations to enhance the capabilities.

So far: We learned the full-state feedback.
If all the states are not available, use an observer
Observer information is reliable enough to use them as real states in the feedback
Combine observer and full-state feedback to design a compensator
Update the compensator to follow a reference trajectory.

Now: What if we have disturbances (external inputs) in the system?

Idea: Estimate the disturbance using the estimator and cancel that signal

Applied Control Engineering

300

## Slide 301

Augmenting the State Space Equations

Applied Control Engineering

301

## Slide 302

Augmenting the State Space Equations

Applied Control Engineering

302

vector

scalar

## Slide 303

Augmenting the State Space Equations

Applied Control Engineering

303

## Slide 304

Disturbance Observer - Example

A = [0 1;-9 0]; B=[0;1];
C = [1 0]; D = 0; 

Ae = [A B; 0 0 0]; Be = [B; 0]; 
Ce = [C 0]; De = 0; 

poles_K = [ -3 -4 ];
K=acker(A,B,poles_K);

desired_poles = [-12 -16 -20];
L = acker(Ae',Ce',desired_poles)' ;               PLANT

Applied Control Engineering

304

Disturbance_observer_constant.mdl

## Slide 305

Disturbance Observer - Example

THE TOTAL SCHEME







					            PLANT

Applied Control Engineering

305

## Slide 306

Disturbance Observer - Example

THE TOTAL SCHEME







					       THE COMPENSATOR

Applied Control Engineering

306

## Slide 307

Disturbance Observer - Example

Applied Control Engineering

307

## Slide 308

Disturbance Observer - Example

Applied Control Engineering

308

## Slide 309

Disturbance Observer - Example

Applied Control Engineering

309

Increase observer gains for a better tracking!

## Slide 310

Disturbance Observer - Example

We can also reject disturbances by designing a good controller.

If we would have used the compensator only to reject disturbances, it would be less succesful.
Let’s not add the estimated disturbance to the input for a second.

Applied Control Engineering

310

## Slide 311

Disturbance Observer - Example

Applied Control Engineering

311

## Slide 312

Reference Tracking with Disturbance Observer

We can extend the whole story with the same reference tracking strategies that we have learned before

Applied Control Engineering

312

## Slide 313

Reference Tracking with Disturbance Observer

Applied Control Engineering

313

## Slide 314

Assignment

Applied Control Engineering

314

## Slide 315

Addition information about Observers

Understanding Kalman filters
https://nl.mathworks.com/videos/understanding-kalman-filters-part-3-optimal-state-estimator--1490710645421.html

Optimal state estimator algorithm
https://nl.mathworks.com/videos/understanding-kalman-filters-part-4-optimal-state-estimator-algorithm--1493129749201.html

Observers for State Space Systems

315

## Slide 316

Observers for State Space Systems

316

## Slide 317

Observers for State Space Systems

317

## Slide 318

Observers for State Space Systems

318

## Slide 319

Observers for State Space Systems

319

Homework

## Slide 320

Observers for State Space Systems

320

Homework

## Slide 321

Feedback Control of Dynamic Systems, 7th edition, Franklin et. al. Global Edition. Pearson.

321

List of resources

## Slide 322

Observers for State Space Systems

322

Homework (Solutions)

## Slide 323

Observers for State Space Systems

323

Homework (Solutions)

## Slide 324

Observers for State Space Systems

324

Homework (Solutions)

## Slide 325

Observers for State Space Systems

325

Homework (Solutions)

## Slide 326

Observers for State Space Systems

326

Homework (Solutions)

## Slide 327

Observers for State Space Systems

327

Homework (Solutions)

