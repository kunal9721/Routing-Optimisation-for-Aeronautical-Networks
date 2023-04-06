# Routing-Optimisation-for-Aeronautical-Networks
This project aimed to optimize the routing path for data transmission between airplanes and ground stations in the North Atlantic.

Numerous planes travel across the North Atlantic daily, as depicted in the image where each black dot symbolizes an aircraft. To furnish internet access toindividuals on board, each plane must determine the most efficient path for transmitting data packets to a ground station (GS) based on one or multipleobjectives that require optimization.

To identify the optimal path for routing data packets, two key metrics must be considered: the overall speed at which data is transmitted and the total delayincurred by each link in the path. The total delay, known as end-to-end latency, is calculated by summing up the delay caused by each link in the path. Forexample, in a routing path that goes from Airplane-5 to Airplane-3 and then to GS-1, with each link having a delay of 50 milliseconds, the end-to-end latencywould be 100 milliseconds. The end-to-end data transmission rate, on the other hand, is determined by the slowest link in the routing path. For example, in arouting path that goes from Airplane-5 to Airplane-3 and then to GS-1, with a data transmission rate of 52.857 Mbps between Airplane-5 and Airplane-3 and43.505 Mbps between Airplane-3 and GS-1, the end-to-end data transmission rate would be 43.505 Mbps. The data transmission rate of a link is determinedby the distance between the communicating airplanes, as outlined in Table 1. As an example, if the distance between Airplane-5 and Airplane-3 is 350 km,falling in the range of 300 km to 400 km, the data transmission rate of the link between these two airplanes would be 52.875 Mbps.

OPTIMISATION PROBLEMS

In this project I have addressed two type of problems for optimizing routing path:

1. Single-objective optimisation:
Routing path having the maximum end-to-end data transmission rate for each airplane that can access any of a GS, either at Heathrow airport (LHR) (Latitude,Longitude, Altitude) = (51.4700° N, 0.4543° W, 81.73 feet) or Newark Liberty International Airport (EWR) (Latitude, Longitude, Altitude) =(40.6895° N, 74.1745°W, 8.72 feet).

2. Multiple-objective optimisation:
Routing path having the maximum end-to-end data transmission rate and minimum end-to-end latency for each airplane that can access any of a GS, either atHeathrow airport (Latitude,Longitude, Altitude) = (51.4700° N, 0.4543° W, 81.73 feet) or Newark Liberty International Airport (Latitude,Longitude, Altitude) =(40.6895° N, 74.1745° W, 8.72 feet).


Methodology

Data Preprocessing: The first step is to preprocess the data. This includes cleaning, normalizing, and formatting the data to ensure that it can be easily analyzed. Specifically, the data should include information about the location of aircrafts, ground stations and any other relevant information that is needed for the routing optimization.

Distance and Transmission Function: Next, define the distance function and transmission function. The distance function is used to calculate the distance between two nodes, and the transmission function is used to calculate the transmission rate between two nodes. The transmission rate is calculated based on the distance between the nodes, the altitude of the aircraft and the type of antenna used at the ground station.

Create Dictionary: Create a dictionary with every possible node. This will be used to store the information about each node, including its location, transmission rate and other relevant information.

Divide Planes: Divide the aircrafts into two lists, one for aircrafts that are in flight and another for aircrafts that are on the ground. This will allow us to apply the routing algorithm to both lists of aircrafts.

Routing Algorithm: Apply the routing algorithm such as Dijkstra or Bellman-Ford algorithm, to both lists of aircrafts and combine the routing path for a single optimization problem. The algorithm should consider the transmission rate, distance, and latency as the parameters to optimize the route.

Multiple Optimization: For multiple optimization problems, use the latency and add 50ms latency for each node in the routing path we got in the single optimization. Also, consider the transmission rate, distance and other relevant parameters that affect the routing optimization.

Ant Colony Optimization: Use the Ant Colony Optimization algorithm for multiple routing optimization and print the best route with the maximum transmission rate and minimum latency.

Evaluation: Finally, evaluate the results by comparing the performance of the proposed methodology with existing methods and analyze the results. This can include metrics such as transmission rate, latency, and routing path length
