
# AlgoQuest

AlgoQuest is an advanced microservices-based code compilation and execution platform designed to deliver functionality similar to popular coding platforms like LeetCode and Codeforces. The architecture is built to ensure high scalability, availability, and performance while providing users with a seamless experience in coding challenges.

## Project Overview

### Microservices Architecture & Scalability
AlgoQuest is architected as a highly scalable microservices-based platform for code compilation and execution. Each component operates independently, ensuring that the system can handle varying loads efficiently. The platform is deployed on AWS, leveraging auto-scaling capabilities to maintain high availability and performance under different usage conditions.

### Dynamic Problem Administration
At the core of AlgoQuest is a sophisticated Problem Admin Service. Built with **JavaScript**, **Express**, and **MongoDB**, this service manages the complete lifecycle of coding problems. It supports CRUD operations, allowing administrators to create, read, update, and delete coding challenges easily. This service incorporates complex test cases and code stubs, facilitating a comprehensive evaluation process for user submissions.

### Advanced Code Execution
The Executor Service is a cutting-edge component developed in **TypeScript** and **Express**. It leverages **Docker** containers to support the execution of code across multiple programming languages, including Java, Python, and C++. This service employs Strategy and Factory design patterns to optimize execution environments and manage various scenarios, such as Time Limit Exceeded (TLE) conditions effectively.

### High-performance Asynchronous Communication
AlgoQuest features a robust Submission Service designed with **Fastify** to handle a high volume of requests with exceptional performance. It utilizes **Redis** message queues for efficient asynchronous communication between services. This design ensures seamless integration between the Submission Service and the Executor Service, allowing for quick processing of user submissions. Additionally, **Socket.IO** is implemented to provide real-time feedback to users, enhancing the platform's interactivity and responsiveness.

### AWS Deployment & Operational Excellence
The entire system is deployed on **AWS**, utilizing various services such as auto-scaling groups, load balancers, and monitoring tools. This deployment strategy ensures optimal performance, fault tolerance, and operational excellence, allowing the platform to scale seamlessly according to user demand.

## Services

AlgoQuest comprises the following four primary services:

1. **AlgoQuest-Evaluation_Service**
   - Responsible for executing code submissions and evaluating the results across supported programming languages.

2. **AlgoQuest-Problem_Admin_Service**
   - Manages the creation, update, and deletion of coding problems, including the setup of test cases and evaluation criteria.

3. **AlgoQuest-Socket_Service**
   - Facilitates real-time communication with users, providing instant feedback and updates during code submission.

4. **AlgoQuest-Submission_Service**
   - Handles the intake of user submissions, processing them through the evaluation service, and communicating results back to the user.

## Tech Stack
- **Languages**: JavaScript, TypeScript
- **Frameworks**: Express, Fastify
- **Database**: MongoDB
- **Containerization**: Docker
- **Real-time Communication**: Socket.IO
- **Message Queue**: Redis
- **Logging**: Winston
- **Deployment**: AWS

## Architecture Diagram

![Architecture Diagram](https://github.com/user-attachments/assets/45980a80-fe63-480a-b8bc-8989f51bc5d4)

This comprehensive setup ensures that AlgoQuest provides a highly interactive and efficient environment for users to engage with coding challenges, fostering both learning and competitive programming.
