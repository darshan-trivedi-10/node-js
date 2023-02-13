# Backend Architecture 

## Introduction
Backend architecture refers to the server-side of a web application, which is responsible for handling the logic and computational processes that power the frontend (client-side) of the application. This includes the database, server-side language and frameworks, and APIs that allow the frontend to communicate with the backend. Backend architecture also includes the infrastructure and systems that support the application, such as servers and network configurations.

## MVC Architecture - (Model-View-Controller)

### Introduction
Model-View-Controller (MVC) is an architectural pattern used in software engineering to separate the concerns of an application into three distinct components: the Model, the View, and the Controller. The key advantage of MVC architecture is that it separates the concerns of the application, making it easier to maintain and scale. The Model, View, and Controller can be developed and tested separately, and changes to one component do not affect the others. This allows for a more modular and maintainable codebase.

![mvc-image-interviewbit](https://github.com/darshan-trivedi-10/Image/blob/main/node-img/Working-of-MVC-800x536.png)

### Components
1. Model: The Model represents the data and the business logic of the application. It is responsible for managing the data and performing operations on it, such as retrieval, storage, and manipulation. It also enforces any rules and constraints on the data.

2. View: The View is the presentation layer that displays the data to the user. It is responsible for rendering the user interface, such as the HTML and CSS, and displaying the data from the Model. It is also responsible for handling any user input, such as button clicks or form submissions.

3. Controller: The Controller acts as a mediator between the Model and the View. It receives input from the user through the View, and then updates the Model and the View accordingly. It also handles any user actions and communicates with the Model to retrieve and update the data.

![mvc-architecture-notes](https://github.com/darshan-trivedi-10/Image/blob/main/node-img/mvc-note.png)

## Folder Setup
- Two types of folder setup
  1. Task Based
  2. Feature Based

![folder-setup-note](https://github.com/darshan-trivedi-10/Image/blob/main/node-img/file-structure.png)

## Repository Layer and Service Layer
The Repository Layer acts as an interface between the application and the database. It is responsible for managing the data and performing operations on it, such as retrieval, storage, and manipulation. The Service Layer acts as a business logic layer that communicates with the Repository Layer to retrieve and update the data. Both the Repository Layer and the Service Layer play a crucial role in MVC architecture by separating the concerns of the application and making it easier to maintain and scale.

## Real-World Example
Consider a simple e-commerce website that allows users to view products, add them to their shopping cart, and purchase them. In this example, the Model could represent the product data, the View could display the products to the user and allow them to add them to their cart, and the Controller could handle the user's actions and update the Model and View accordingly. The Repository Layer could handle the database operations for retrieving and storing the product data, while the Service Layer could
![flow](https://i.stack.imgur.com/mx1G1.png)
