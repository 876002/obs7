# OBS7 Homework Assignments Solutions

## Slide 1

Write a Matlab function isStable(A,B,C,D)
that returns the boolean value (true or false) if the system is stable.


Tips:
Check your function with   >>  isStable([-1 0;0 -2],[1;1],[1 0],0)   in the command window
Don’t use isstable built-in function.
Use eig(A) to get access to the eigenvalues.
Don’t write everything in a script, but in a function. (Click on New->Function)


Solutions: see last slide of the ppt

Observers for State Space Systems

1

Assignment = 15 min.

## Slide 2

function [ boolean ] = isStable( A,B,C,D)
 
	E = eig(A);
 
	positive_eigenvalues = E(E>0);   %Make E consist of only the 					positive elements
 
	if any(positive_eigenvalues) == 1
    
    		boolean = 0;
    
	else 
    
    		boolean = 1;

	end
end

Observers for State Space Systems

2

Assignment solution isStable.m

## Slide 3

Observers for State Space Systems

3

## Slide 4

Observers for State Space Systems

4

Homework (Solutions)

## Slide 5

Find the state space representation of the following two cart system with friction on the wheels.

Observers for State Space Systems

5

Homework

## Slide 6

Observers for State Space Systems

6

Homework (Solutions)

## Slide 7

Homework (Solutions)

Observers for State Space Systems

7

## Slide 8

Homework (Solutions)

Observers for State Space Systems

8

## Slide 9

Homework (Solutions)

Observers for State Space Systems

9

## Slide 10

Assigment

Observers for State Space Systems

10

## Slide 11

Homework (Solutions)

Observers for State Space Systems

11

## Slide 12

Homework (Solutions)

Answers

Observers for State Space Systems

12

Yes
No
Yes because the unstable pole can be moved
No because not all the poles are allowed to be freely placed

## Slide 13

Homework

Observers for State Space Systems

13

## Slide 14

Homework (Solutions)

Observers for State Space Systems

14

## Slide 15

Homework (Solutions)

Observers for State Space Systems

15

## Slide 16

Homework (Solutions)

Observers for State Space Systems

16

## Slide 17

Homework

Observers for State Space Systems

17

## Slide 18

Solution

Observers for State Space Systems

18

## Slide 19

Homework (Solutions)

Observers for State Space Systems

19

## Slide 20

Homework (Solutions)

Observers for State Space Systems

20

## Slide 21

Homework (Solutions)

Observers for State Space Systems

21

## Slide 22

Homework (Solutions)

Observers for State Space Systems

22

## Slide 23

Homework (Solutions)

Observers for State Space Systems

23

## Slide 24

Homework (Solutions)

Observers for State Space Systems

24

## Slide 25

Homework (Solutions)

Observers for State Space Systems

25

## Slide 26

Homework (Solutions)

Observers for State Space Systems

26

## Slide 27

Homework (Solutions)

Observers for State Space Systems

27

## Slide 28

Homework (Solutions)

Observers for State Space Systems

28

## Slide 29

Homework (Solutions)

Observers for State Space Systems

29

## Slide 30

Homework (Solutions)

Observers for State Space Systems

30

## Slide 31

Homework (Solutions)

Observers for State Space Systems

31

## Slide 32

Homework (Solutions)

Observers for State Space Systems

32

## Slide 33

Homework (Solutions)

Observers for State Space Systems

33

## Slide 34

Homework (Solutions)

Observers for State Space Systems

34

## Slide 35

Homework (Solutions)

Observers for State Space Systems

35

## Slide 36

Homework (Solutions)

Observers for State Space Systems

36

## Slide 37

Homework (Solutions)

Observers for State Space Systems

37

## Slide 38

Homework (Solutions)

Observers for State Space Systems

38

## Slide 39

Homework (Solutions)

Observers for State Space Systems

39

## Slide 40

Homework (Solutions)

Observers for State Space Systems

40

## Slide 41

Homework (Solutions)

Observers for State Space Systems

41

## Slide 42

Homework (Solutions)

Observers for State Space Systems

42

## Slide 43

Homework (Solutions)

Observers for State Space Systems

43

## Slide 44

Homework (Solutions)

Observers for State Space Systems

44

## Slide 45

Homework (Solutions)

Observers for State Space Systems

45

## Slide 46

Homework (Solutions)

Observers for State Space Systems

46

## Slide 47

Homework (Solutions)

Observers for State Space Systems

47

## Slide 48

Homework (Solutions)

Observers for State Space Systems

48

## Slide 49

Observers for State Space Systems

49

Homework (Solutions)

## Slide 50

Observers for State Space Systems

50

Homework (Solutions)

## Slide 51

Observers for State Space Systems

51

Homework (Solutions)

## Slide 52

Observers for State Space Systems

52

Homework (Solutions)

## Slide 53

Observers for State Space Systems

53

Homework (Solutions)

## Slide 54

Observers for State Space Systems

54

Homework (Solutions)

