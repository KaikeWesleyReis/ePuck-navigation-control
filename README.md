# BIR Challenge
This code was created using Lua programming language in V-REP Software. The challenge consist in create a navigation system to ePuck robot model allowing him to:
- start from Start Point
- follow a black line as route
- avoid any obstacle present in his route
- follow the black line after avoid a obstacle 
- finish when ePuck gets to Ending Point
*PS*: To works correctly, is necessary to start with the light sensors in a white field.

### Test Environment
Here you can see the environment here this navigation system was created to face:
![env](https://user-images.githubusercontent.com/32513366/52373421-be922380-2a41-11e9-82a9-4f038d66fd5f.PNG)

### Obstacles Type, Start Point and End Point
Here, you can see the start point proposed and the End Point respectively:
![startend](https://user-images.githubusercontent.com/32513366/52374926-a4f2db00-2a45-11e9-9272-9ae687491ad1.png)

and here there are the two main types of obstacles:
![obstacles](https://user-images.githubusercontent.com/32513366/52373562-1fb9f700-2a42-11e9-892f-3e57d9562678.PNG)

To improve my navigation system quality, several combinations from those obstacles types was putted in the environment (angle and putting together), increasing the difficulty for ePuck to avoid obstacles and come back to your route.

### Challenges to create this navigation system
- Learn Lua programming code to perform this task;
- Improve my knowledge related to **if-else**,**if-else if** and **if-else if-else**. A wrong use of those statements can break your navigation system decision management;
- Understand how the proximity and light sensors works in ePuck model as your engines located the in left and right wheels;
- Find online material related to v-rep software to help in this task;
- Start to understand how to do reverse engineering in programming codes.

### Main Improvements compared to Demo Navigation System
- A well organized code with commentaries and a explicit declaration of hyper parameters from navigation system;
- A more precise division of routines: Look for a line, follow the line in a normal way or after avoiding a obstacle and so on. Different from the demo;
- Follow line algorithm in general was improved compared the old one;
- Avoid Obstacles was improved and tested with different combinations in the environment;
- A good routine to get the line after avoiding a obstacle;
- Vision's Treshold Improvement.

### Possible Issues and Community help
Well, the code is not perfect. There are some issues that can happen:
- Putting two obstacles too close i.e. you don't give a space to ePuck to get a line after avoiding the first obstacle and then avoid the second obstacle can break the routines;
- The routine to get a line when start doesn't respond well to some situations, in fact this was the most problematical part to create this system. The best scenarios where works fine is when the robot get diagonally over the the line. Unfortunaley I took two days trying to solve this issue and I did not figure out how can I take perfectly the line, independent of any angle.
