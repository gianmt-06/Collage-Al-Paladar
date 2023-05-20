# Collage Al Paladar

This is a university project developed as a team with my partner, [@Alejo-Rodri](https://github.com/Alejo-Rodri), for the subject of Data Structures. It is about a distributed system using RMI for a restaurant.

This project consists of 4 modules:

- Administrator: responsible for registering users and dishes.
- Operator: responsible for registering and validating users, taking orders, and being able to modify or cancel them.
- Kitchen: implements a priority queue to organize orders and a system that manages the availability of stoves in the kitchen.
- Delivery: implements an algorithm to calculate the closest route the delivery person should take to reach their destination and deliver all the orders.

For more details about the project, such as the data structures used, implemented algorithms, or technologies utilized, feel free to contact any one of us.


Technologies used in the project include:

- Java: The programming language used for the project's implementation.
- RMI (Remote Method Invocation): A Java API that enables communication between distributed systems.
- JavaFX: A Java library used for building graphical user interfaces (GUIs) for desktop applications.
- CSS: Cascading Style Sheets, a language used for styling the visual elements of the application.
- Figma: A web-based design and prototyping tool used for creating user interface designs and collaborative design work.
- FXML: A markup language used in JavaFX for defining the structure and layout of user interfaces.

## Admin Module
<p>
  In this module, we can observe the way users are added, their information is displayed, and the implemented search algorithm             (Levenshtein distance). RMI Server
</p>
<div align="center">
  <img align="center" alt="adminModule" src="admInterface.gif">
</div>

## Operator Module
<p>
  This module communicates through RMI with the server to obtain client information or register a new client. It can also send the order to the kitchen to start the cooking process. In this module, the delivery price is calculated based on the distance of the delivery location. The distance is obtained through a custom implementation of an algorithm that uses a .txt file with a syntax referring to its adjacency list to return a graph. Later, Dijkstra's algorithm is used to find the shortest route from the restaurant to the desired location.
</p>
<div align="center">
  <img align="center" alt="kitchenModule" src="operatorInterface.gif">
</div>

## Kitchen Module
<p>
  In this module, an algorithm was implemented to assign delivery priorities and subsequently organize them in a priority queue. These priorities depend on the user's rank and the delivery distance of the order from the restaurant. Additionally, an algorithm was implemented in this module to assign a stove to each dish entering the kitchen based on availability. The stoves were divided as follows: four stoves for dishes with a cooking time of 10 minutes and twelve stoves for dishes with a cooking time less than 10 minutes.
</p>
<div align="center">
  <img align="center" alt="kitchenModule" src="kitchenInterface.gif">
</div>
