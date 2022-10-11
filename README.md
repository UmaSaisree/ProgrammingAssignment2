# Team Members:
Pravallika Maddukuri - UFID : 5980-7014<br/>
Sai Siddharth Upadhyayula - UFID : 74599449<br/>

# Description
This project deals with the convergence of gossip algorithm, in this algorithm we compare the convergence of gossip and pushsum algorithms, in pushsum algorithm every actor stores two variables s and w, so using these values we find the ratio of s/w each time, and terminate the algorithm when s/w did not change more than 10^-10, in three consecutive times.

# Execution Steps - 

Firstly we are having 4 files. 
We have to compile these files using the command c(filename). Then beam files will get generated 
II. 	Then we have to execute the project by directing to the current folder’s path in the terminal, by using the following command 
main: start(“<no.of workers>”,”<name of the topology>”,”<name of the algorithm”>) 
we are having the following topologies 
•	Line 
•	Full 
•	3D 
•	Imperfect3D 
 
We are having the following algorithms 
•	Gossip 
•	pushsum 


# Report Questions

2.	The highest working condition 
a)	What algorithms and topologies are working 
All the algorithms and topologies are working with each other i.e., Gossip algorithm is working with line, full, 2D and Imp3D topologies and the same with the pushsum algorithm. 
b)	Maximum number of Workers used? 
        
The maximum number of workers used is varied from algorithm to algorithm for gossip algorithm for line topology we used 8192 as the maximum no of workers and 4096 for remaining other topologies, and 4096 for all topologies in pushsum algorithm 
        
      | Algorithm | Topology | No.of workers | Wall Clock Time |
      | --------- | -------- | ------------- | ----------------|
      | Gossip    | Line     | 8192    | 3292                  |
      | Gossip    | Full     | 4096   |  1147820               |
      | Gossip    | 2D       | 4096    | 19625                 |
      | Gossip    | Imp 2D   | 4096   | 20353                  |
      | PushSum   | Line     | 4096    | 3290                  |
      | PushSum   | Full     | 4096    | 90185                 |
      | PushSum   | 2D       | 4096    | 38199                 |
      | PushSum   | Imp 2D   | 4096   | 987                    |
        
   Line Topology for Gossip Algorithm     
 <img width="1440" alt="1" src="https://user-images.githubusercontent.com/57837608/194992998-2e6422b7-bebe-4648-849b-a17f73938c15.png">
        
Full Network Topology for Gossip Algorithm
<img width="1440" alt="2" src="https://user-images.githubusercontent.com/57837608/194993059-e663271c-5bcb-4836-ac03-f24c74e80765.png">
        
2D Topology for Gossip Algorithm
<img width="1440" alt="3" src="https://user-images.githubusercontent.com/57837608/194993080-74ba472a-efca-4104-a963-b0f48bf7b371.png">
        
Imp 3D Topology for Gossip Algorithm
<img width="1440" alt="4" src="https://user-images.githubusercontent.com/57837608/194993103-0f42de02-a0d4-4ccb-89c2-657f5faf0e46.png">
        
        Line Topology for PushSum Algorithm
<img width="1440" alt="5" src="https://user-images.githubusercontent.com/57837608/194993124-af48a123-e060-46ec-bacb-57cd0d1cf807.png">
        
        Full Network Topology for PushSum Algorithm
<img width="1440" alt="6" src="https://user-images.githubusercontent.com/57837608/194993134-530075d0-499e-4902-9843-f2b033d342c6.png">
        
2D Topology for PushSum Algorithm
<img width="1440" alt="7" src="https://user-images.githubusercontent.com/57837608/194993146-8294f44a-4cad-4393-ade6-9110826dedad.png">
        
Imp 3D Topology for PushSum Algorithm
<img width="1440" alt="8" src="https://user-images.githubusercontent.com/57837608/194993163-bc8f8d2d-c116-4868-8352-9ff51383bf8f.png">

        
 
 
3.	Observations and final output 
We have executed our project using the powers of 2 number of workers i.e, from 2,, 8 and so on mostly till 4096 and 8192. The observations are like the following, we used wall clock for calculating the time. By the observation from the graphs we can infer that for each topology for gossip algorithm we can observe that 2D and Imp3D lines almost looks similar in a same manner, till two thousand workers with a slight change at the end, whereas the line topology for gossip algorithm’s graph has been rising constantly without any high deviations, and the timing for the full topologies are very less compared to the other topologies wth a constant growth. 
 
For Pushsum Algorithm, the line topology has the highest time recorded with a constant growth in time frame, when compared with no.of workers, and next comes the 2D topology for the highest time, the Imp3D and full topologies for pushsum have almost the same time frame till 2K. 


 



