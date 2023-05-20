# Collage Al Paladar

This is a university project developed as a team with my partner, [@Alejo-Rodri](https://github.com/Alejo-Rodri), for the subject of Data Structures. It is about a distributed system using RMI for a restaurant.

This project consists of 4 modules:

- Administrator: responsible for registering users and dishes.
- Operator: responsible for registering and validating users, taking orders, and being able to modify or cancel them.
- Kitchen: implements a priority queue to organize orders and a system that manages the availability of stoves in the kitchen.
- Delivery: implements an algorithm to calculate the closest route the delivery person should take to reach their destination and deliver all the orders.

## Admin Module
<div align="center">
  <p>In this module, we can observe the way users are added, their information is displayed, and the implemented search algorithm (Levenshtein distance). RMI Server</p>
  <img align="center" alt="adminModule" src="admInterface.gif">
</div>

## Operator Module
<div align="center">
  <p>This module communicates through RMI with the server to obtain client information or register a new client. It can also send the order to the kitchen to start the cooking process. In this module, the delivery price is calculated based on the distance of the delivery location. The distance is obtained through a custom implementation of an algorithm that uses a .txt file with a syntax referring to its adjacency list to return a graph. Later, Dijkstra's algorithm is used to find the shortest route from the restaurant to the desired location.</p>
  <img align="center" alt="kitchenModule" src="operatorInterface.gif">
</div>

## Kitchen Module
<div align="center">
  <img align="center" alt="kitchenModule" src="kitchenInterface.gif">
</div>
