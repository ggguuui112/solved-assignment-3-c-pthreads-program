Download Link: https://assignmentchef.com/product/solved-assignment-3-c-pthreads-program
<br>
Assignment 3- C++ Pthreads program

AimThe objective of this assignment is to apply the concepts of threading by developing a simple C++ Pthreads program to discover the surroundings and the shortest path in a 2D maze

BackgroundThis assignment requires you to write a multi-threaded C/C++ “Pathfinder” program to discover the surroundings of a jungle maze. Each [x, y] location in the maze represents a ‘grid area’ of the jungle terrain. A particular gird area could be

“impassable”             (rep. by ‘#’ barrier) ,

containsdanger       (rep. by ‘X’ danger area)

·clear,                          (i.e. allows you totravel)

An example of the jungle maze will be provided to you (see <strong>Appendix A</strong>,‘mazedata.txt’).Your objective is to explore as much of the jungle maze terrain as possible, and mark the discovered area as barrier (‘#’), or danger (‘X’) accordingly.When your program terminate, it should output a map of the explored jungle maze, as well as 1 ‘safe’ path, to traverse from Start to End locations.

Task RequirementsA)  At startup, your program should read in the 2D maze configuration (“mazedata.txt”) which stores the information about the maze dimensions, barriers, start and end locations. Please refer to <strong>Appendix A</strong> for an example.

B)  For the purposes of testing your program, a sample of what information should be output is shown in <strong>Appendix </strong>C)  Before you start developing your program, you should take some time to review the output, and analyze the requirements of the Pathfinder program.D)  Your program should have <strong>at least</strong> 2 threads, each thread attempting to explore surrounding locations to discover whether it contains a barrier (‘#’) or danger (‘X’).

E)  Impt1 : your program should maintain a global Maze resource or variable, holding information about all the barriers or danger areas uncovered by your exploring threads!

F)  Impt2 : when a particular thread has encountered a barrier (‘#’) or danger (‘X’), it should …

Recordthe path (history of point locations) it has traversed, since the Start Location, to reach the barrier / danger areas, and locations of barrier / danger should be marked on your ‘global Maze resource’

<strong>The thread ‘loses its life’ (i.e. should be destroyed) if it has encountered adanger area (‘X’) !!</strong>G)  Whenever a thread is destroyed, your program should create another replacement thread, to traverse the jungle maze beginning from the Start Location again. But this time, it should access the ‘global Maze resource’ to learn and avoid the barriers and danger areas discovered by its predecessor threads!

H)  In this way, the ‘sacrifice’ of the destroyed threads are not in vain, as its knowledge (of locations of the barriers / danger areas) have been recorded in the ‘global Maze resource’ that can be accessed by future generations ofcreated threads to aid their survival in order to discover a path to End Location!I)    As you probably guess by now, the access to the ‘global Maze resource’ should be protected via usage of mutex locks. Whether a thread is:

Updating its discovery of the path to barrier / danger areas  OR

Accessingthe ‘global Maze resource’ to learn about the discovered locations of the barriers / danger areas

Only 1 thread can access it at any one time!J)   Once the program is completed and tested to be working successfully, you are highly encouraged to add on “new features” to the program that you feel are applicable to the task of finding the shortest path thru a maze. Additional marks may be awarded subject to the relevancy and correctness of the new functionalities.

K)  Your program should be written in C++, and using the library functions available in header file ‘pthread.h’, to handle all aspects of thread creation, management and synchronization.

L)   To encourage good program design, you should consider using different *.cpp class files to encapsulate groups of related methods/functions.

Additional Resources

<ul>

 <li style="list-style-type: none;">

  <ul>

   <li>After all students have gone through this document, your tutor will hold a special session to discuss / elaborate on the requirements of this assignment.</li>

  </ul></li>

</ul>

<ul>

 <li>In addition, your tutor will hold a Q &amp; A sessions to clarify any issues/doubts you may have on the analysis and design of this multi-threaded program. To ensure a fruitful session, all students must come prepared with their list of questions, so that everybody’s time is efficiently utilized.</li>

</ul>

Summaryof implementation of each module in your program

A program demo/evaluation during lab session. You must be prepared to perform certain tasks / answer any questions posed by the tutor.