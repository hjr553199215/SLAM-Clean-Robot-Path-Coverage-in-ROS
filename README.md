# SLAM-Clean-Robot-Path-Coverage in ROS
# Summer Holiday in BIT for Clean Robot


# Path Planning：

（1）Basic idea：map segmentation

（2）The concept of Cell is important in Coverage. It represents the minimum unit in the map. For some situations, the developers can determine the shape of Cell for any kinds of agents. Square is the most common one for coverage.

（3）For the cost_map library, grid map is the important format for avoiding the obstacles. In the common map, we will describe the position by (x,y). But in the grid map, we describe the position by the index of a cell. For example, the (x,y) in the common map will be converted into the (x*width+y) in grid map.

（4）2019.07.06 the demo has been tested successfully, but it still shows some problems in this test:

     a.There is some long lines in the costmap which has been planned. It is impossible for the agent to run.
     b.In this algorithm, a lot of turns were produced, that will cost a lot of energy for our agents.

（5）parameters adjustment

（6）For solving the self-locking problem , I add a new method in the original algorithm. A* algorithm(point-to-point path plan) is adopted for this problem.

（7）Reducing the number of turns. Change the scoring mechanism.

（8）If you want to run this program on your devices. You need to install some dependences. 

I show the results of this program as follows:

![two bears](https://github.com/hjr553199215/SLAM-Clean-Robot-Path-Coverage/blob/master/path_29.png)

![two bears](https://github.com/hjr553199215/SLAM-Clean-Robot-Path-Coverage/blob/master/path_coverage.png)

After adjusting the algorithm, the number of turns has been reduced substantially. But the path on oblique section is not ideal. This phenomenon may be caused by the meshing of our map.

Following is the result of reducing turns:

If you find some disadvantages about this program, or you have a better idea to achieve the coverage and improve this program, welcome to discuss!
