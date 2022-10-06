# Web Application Structure
In this training, we'll be learning how to build full-stack web applications.
What does this mean?
Well, full-stack refers to the fact that we will be able to build all of the main components:
- Database
- Back end (server)
- Front end (client)
Most importantly, we need to understand how these components interact with one another.

## Database
The database is where all of your data is stored. This data is anything that you'd want to keep even after somebody stops using the application and comes back. This might include things like:
- usernames/passwords
- addresses
- inventory (food/shop items)
- color/size options
- item types
- order/delivery statuses

These might be things the user wants to look at or things that are necessary to make sure the user sees what they're supposed to see.
During training, we'll be using Oracle SQL for our database.

## Back End (Server)
The back end is where the so-called "business logic" of an application occurs. This can be a number of things, such as:
- getting the data from a database to the user
- calculations like how much someone owes on something or how much money they have left in an account
- changing a status to "delivered"
- authentication
- input validation

The main role of the back end is that it acts as a bridge between the database and what the user sees - it handles everything in between, and it needs to be able to both communicate with the database and send information to the front end.

During training, we'll be using Java for our back end, plus (initially) Hibernate to interact with the database and Javalin to accept requests from the front end. Eventually, we will replace both Hibernate and Javalin with the Spring framework.

## Front End (Client)
The front end is what the user interacts with. Its main job is to show the user the correct things and respond to what the user wants. This could include things like:
- show the user all of the shop inventory
- allow the user to log in
- allow the user to buy something when they click a button

In order to provide this functionality, the front end needs to make requests to the back end - essentially, the user lets the front end know what they want, and the front end tells the back end "here's what the user needs right now." Once it gets a response, it can show the user the correct thing.

During training, we'll initially be using plain HTML, CSS, and JavaScript for our front end. Eventually, we will be using the Angular framework with TypeScript in order to get more out of these languages.

## Example
CatApp: A web application used for adopting cats.

Functionalities:
1. A user can register an account.
2. A user can log in.
3. A user can view the available cats.
4. A user can adopt a cat.
5. A user can view the cats that they've adopted.

Entities:
- Cat*
- User*
- Status (a cat can be available, adopted, etc.)
- Breed (cat breeds)
- Role (a user can be a regular user, an employee, a foster, an admin, etc.)
- Special Need (special needs that a cat could have like blindness, FIP, etc.)

*These are the ones that are absolutely necessary - the others are helpful, but not necessary (we'll talk about it later).

Flow of the application:
1. Functionality/Story 1:
    1. A user will enter their information on the front end and click a "register" button.
    2. The front end will send the information and tell the back end "hey, add this user to the database, please."
    3. The back end will get the information and add it to the database.
    4. The database now has the user's information and the back end will tell the front end "hey, let the user know that they registered successfully, please."
2. Functionality/Story 2:
    1. A user will enter their username and password and click a "log in" button.
    2. The front end will send the information and tell the back end "hey, this user would like to try to log in."
    3. The back end will check if that information is in the database.
    4. If it is, it will send the rest of the user's information and tell the front end "hey, this user is good to go, they can be logged in now."
    5. If it isn't, it will tell the front end "hey, that user doesn't exist, please let them know that information is wrong."
3. Functionality/Story 3:
    1. A user will go to a page to see the available cats.
    2. The front end will tell the back end, "hey, please give me all of the available cats that are in the database right now."
    3. The back end will grab the cats from the database and make sure that it only sends back the available ones.
    4. The front end will take the cats that it got and show them to the user in a nice format.
4. Functionality/Story 4:
    1. A user will see a cat that they like and click an "adopt" button for that cat.
    2. The front end will tell the back end, "hey, this user wants to adopt this particular cat."
    3. The back end will make sure that that cat is available to be adopted.
    4. The back end will then tell the database to update that cat's status to adopted.
    5. The database is updated and the back end will tell the front end, "hey, that cat is adopted by that user now."
5. Functionality/Story 5:
    1. A user will go to a page to see their cats.
    2. The front end will tell the back end, "hey, please give me the cats that are owned by this user."
    3. The back end will ask the database for any cats that are adopted by the user and return those to the front end.
    4. The front end will show those cats to the user, or give them a special message if they don't have any cats yet.

# Your Task
Create a project plan similar to the CatApp example above. You'll need to decide:
1. Five things that your website will do (functionalities)
2. Which entities your website will need to store
3. The flow between front end/back end/database for each functionality/user story

You'll then present this plan to the trainer and cohort. You can present it in whatever form works best for you (powerpoint, diagrams, etc.)

The main goal of this is for you to understand the different components of a full-stack web applications and how they interact with each other when you're actually using a website.
