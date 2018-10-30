# X-Team 108 Follow the Leader

See https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#code for tips on using *Markdown* tags to format __.md__ files

## Goal

Work as a team to create a project proposal for your X-team to complete together.
The project does not have to be extremely difficult,
but there must be work to do for each member of your team.
You may reference figures using "See figure 1".  
Be sure to submit corresponding image files, i.e. figure1.png (or figure1.jpg) for each figure.

## Grading: To earn full credit, your team's proposal must include:

* (md) documentation: [this file] describing purpose and use of your program

* Description of a program that has:

  ** a main Java program class in a file named Main.java
  
  ** a custom data structure designed and built by your team
  
  ** comprehensive testing of individual units
  
 Caution: You are not being asked to implement this program, at least not yet. 
 We just want your group to make a proposal or pitch for your program.
 
 Tip: Your custom data structure can be composed of or extensions of data structures that you have learned and used in previous programming assignments.  We're looking for decisions about how to build a high-level data structure that will likely have lower-level components.

## Problem Description

Briefly describe a problem that your team would like to solve.  
Describe at a high level a program that could solve that problem.

When it comes to choosing a leader in a new project group, it is ususally the case true that the most extroverted member is chosen because of their confidence. However, it has been reported that introverts make great leaders as well in some settings. Unfortunately, they rarely get chosen as their quietness and reserved characteristics do not get them attention needed to be picked. There are also some cases that all the members are introverts who do not think themselves as a leadership material(40 - 60% of population are introverts!). For instance, in our project team, there was nobody volunteering to be a team leader.  
To be able to pick the most suitable leader in a more objective manner, we would like to build a program to systematically choose the most appropriate member as a leader. 
In our program we evaluate each member's desirability as a leader based on 1) attendance 2) contribution. We would also keep track of who's doing their part, and re-evaluate each member as needed! 

## Questions to answer for Exercise #2

1. Name: Give your project proposal a name (and edit the top line of this file)

  **Follow the Leader**


2. Output: Describe the output your program will produce.  Include and example format of the output produced.
The name of the top member with some statistics on the progress/performance in the team.
i.e.  
* We calculate the input of each member's attendance rate and the percentage of their completion in given assignment.
* Last Name, First Name  
* Attendance: x/y meetings  
* Notable Contributions: x, y, z  

3. Input: Describe the data that is needed to solve your problem. Include an example format of the input data.

* member name (string)  
* meetings attendance (boolean)
* tasks completion (boolean)
* names of tasks(string)
* date of meetings (date)

4. User Interface: Describe a user interface for your program.    

![alt text](https://github.com/yukiko0219/teamExercise/blob/master/figure1.jpeg)

Use text menus or a simple graphic user interface.
In the main page, there will be a menu where you can select "meetings, tasks, members, etc." that leads to a matrix of all the tasks/meetings and the memebers' names where each memeber can check if they have attended the meetings or done the tasks. Attendance and task completion would also be input into these tables. Data input into this page will be brought into the algorithm to decide who the next leader will be. 
Please see the figure 1.

5. Types List: Break your solution idea down into units that you think can be implemented with a single class.

**_class Leader_**  
this class keeps track of the progress of different members of the team and picks the member most suited as a leader  
*fields*  
* PQ members
Priority Queue to pick the member node with the best performance/ nodes will be the inner class Memebrs which stores informations on the members and their perfomances （if this priority queue is only for our xteam, we can set members as class fields: every change of the information can be updated to the class immediately）

*  ArrayList<Meeting> meetings
 Arraylist to store the meetings
 
 *  ArrayList<Task> tasks
 Arraylist to store the tasks

*methods*  
*  set_up(): setup the UI for the program/restore the data from last session from the separate data.txt file  
Testing: Prepare data.txt with different set of data inside, and test if the set_up generates the UI accordingly.  

*  get_info(): Get the informations on the input data(Meeting assignments/completions e.t.c) from the stdin and store/update the info on a separate data.txt file   
Testing: Prepare various set of input data and test if the data.txt files are generated accordingly  

* update(): update the nodes on of priority queue based on new data from data.txt  
Testing: Prepare different set of data.txt and test if update() update the PQ accordingly. Use dequeue() to check if the memebers are stored in the appropriate order.

* assign_meeting(date date) :assign meetings on a specific date   
Testing: prepare different set of dates and test if assing_meeting update ArrayList<Meeting> meetings accordingly

* assign_tasks(string member_name, string taskname) :assign a specific task to a member  
Testing: prepare different set of tasks with different memebers assigned. Test if assign_task(member_name, taskname) updates ArrayList<task> tasks accordingly.

* pick_leader(): returns the Member object with the best performance, according to the algorithm in calculate_weight()   
Testing: Create PQ of memebrs with different performance rate, test if the memebr with the best performance is chosen.


**_inner class Member_**  
This inner class stores the information of each member  
*fields*  
* String firstname, lastname  
* ArrayList<Task> assigned(list of assigned tasks )
* ArrayList<Task> completed(list of completed tasks)
* double meetingAttendanceRate 

*method*  
* private calculate_weight(): Calculate the weighted average of each member's performance(20% on attendance, 30% compleetion rate of the tasks...)   

**_inner class Meeting_**  
This inner class stores the information on a meetings  
*fields*  
* string meetingname  
* data date  
* Members[] (keeps track of who attended the meetings/empty by defalt upon the meeting assignment  

**_inner class Task_**  
This inner class stores the information on a task  
* Member assgined (member object of the member who was assigned this task)  
* String task name  
* boolean complete (true if completed, false by defaul on the task assignment)  

Name each interface or class and briefly describe its function or purpose.


## Edit and Submit this file and any figures referenced by this document.

