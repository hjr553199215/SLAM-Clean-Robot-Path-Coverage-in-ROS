# SLAM-Clean-Robot-Path-Coverage
Summer Holiday in BIT for Clean Robot


Path Planning：

（1）Basic idea：map segmentation

（2）The concept of Cell is important in Coverage. It represents the minimum unit in the map. For some situations, the developers can determine the shape of Cell for any kinds of agents. Square is the most common one for coverage.

（3）For the cost_map library, grid map is the important format for avoiding the obstacles. In the common map, we will describe the position by (x,y). But in the grid map, we describe the position by the index of a cell. For example, the (x,y) in the common map will be converted into the (x*width+y) in grid map.
