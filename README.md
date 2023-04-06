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
