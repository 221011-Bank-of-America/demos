# Project 1.5: Banking Application with Hibernate and Persistence

* Assigned Date: Monday **10/31/2022**
* Due Date: **11/11/2022**

# Description
Building upon your Project 1, implement Hibernate as your ORM to persist all data to an Oracle RDBMS.

## Tech Stack
- Oracle Database
- Hibernate ORM
- Mockito
- Java 8 (or higher if you so choose)
- Maven
- JUnit 4
- Log4J

## Requirements
- Use JPA nnotations such as `@Entity, @Column`, etc. to declare your persistent classes

- Create a DAO layer for each persistent entity, which calls upon Hibernate's Session methods (e.g `.save(), .delete()`, etc)

- Implement the DAO design pattern including `model`, `service`, and `dao` layer
 
- Use JPA annotations over the properties of each persistent class to map numerical relationships between entities (`@OneToMany`, `@ManyToMany`, etc)

- Implement Mockito for Unit testing the Service layer
  - Aim to achieve 80% Test Coverage of the Service layer

<br>

## Presentation
- Explain your ERD (Entity Relationship Diagram) and proove persistence in your demonstration
- Clear, concise, and professional communication during the project presentation
- Ability to communicate clear answers to fully address questions asked about the project
- Logical flow to the project presentation

<br>

# Frequently Asked Questions
1. When is the project due? 

    >A: Friday November 11th, 2022. 

2. Is there a code freeze? 
    >A: It is recommended that you institute your own code freeze at least a day before the project presentations. However, this is a recommendation only; it will not be enforced. NOTE: The code that will be evaluated by your trainer will be the code you last pushed to your repository BEFORE the time set for project presentations. Code submitted while presentations are on-going will not be evaluated. 

3. What happens if I break my project that was mostly working right before the due date? 
    >A: **As you should have been regularly pushing code to your repository** you should be able to roll back to previously working version. If you have not regularly pushed your code and do not have a working commit to return to you will need to present the state of your application in its current form. 

4. Who will be evaluating the project? 
    >A: Your trainers will be the ones providing the full evaluation of your projects. However, the QC team will also be present at presentations to ask questions about your project and consult with your trainer. 

5. Are we allowed to collaborate with others on our projects? 
    >A: Collaboration is encouraged. By helping others, and in turn posing good questions, you will become a stronger developer. Hopefully you will work together to solve the problems presented in this project.  However, you should still be ultimately designing the project yourself. Straight copy/pasting of another person's code is considered plagiarism and NOT allowed. NOTE: Code provided in demos by your trainers is not subject to plagiarism concerns. *Feel free to copy/paste and edit your trainer's code as necessary to suit your projects.*
