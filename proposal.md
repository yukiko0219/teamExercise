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

In our team, there was nobody volunteering to be a team leader, so we would need a systematic way to choose the most appropriate member as a leader. 
 It would probably be a priority queue that weighted each member of a team on 1) attendance 2) contribution 3) leadership 4) team votes etc. and you could constantly update it to keep track of who's doing their part! I think this would be helpful not only for us, but for other teams in the class and across the world!

## Questions to answer for Exercise #2

1. Name: Give your project proposal a name (and edit the top line of this file)

Follow the Leader


2. Output: Describe the output your program will produce.  Include and example format of the output produced.
The name of the top member with some statistics on the progress/performance in the team.
i.e.
Last Name, First Name
Attendance: x/y meetings
Notable Contributions: x, y, z

3. Input: Describe the data that is needed to solve your problem. Include an example format of the input data.

class Member node 
fields
1. member name (string)
2. meeting attendance rate (double)
3. tasks assigned (string[])
4. tasks completed(string[])

class method
calculate_weight() :calculates the weighted average of member's performance based on meeting attendance rate and task completion rate

4. User Interface: Describe a user interface for your program.  Use text menus or a simple graphic user interface.
In the main page, there will be a menu where you can select "meetings, tasks, members, etc." that leads to a matrix of all the tasks/meetings and the memebers' names where each memeber can check if they have attended the meetings or done the tasks. Attendance and task completion would also be input into these tables. Data input into this page will be brought into the algorithm to decide who the next leader will be. 


5. Types List: Break your solution idea down into units that you think can be implemented with a single class.
ADT: Priority Queue to pick the member with the best performance/ nodes will be the memebrs with informations on their perfomances

get_info(): Get the info from the stdin

calculate_weight(): Calculate the weighted average of each member's performance(20% on attendance, 30% compleetion rate of the tasks...)

update(): update the nodes on of priority queue based on new statistics

This would also include the class Member node listed above.

Name each interface or class and briefly describe its function or purpose.


## Edit and Submit this file and any figures referenced by this document.

