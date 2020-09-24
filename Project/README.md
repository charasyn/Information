<h1 align='center'>🍿 An Extreme Course Project: SeetGeek 🍿</h1>

<p align='center'>CISC 327  -  Fall 2020</p>


## 💺 Project Teams

You are to form a team of two to four (preferably four) people to design, implement, document and deliver a two-part software product.  All phases should follow the eXtreme Programming philosophy as much as it applies - in particular, 

- continuously maintained test suites as requirements and quality control
- pair programming of all code
- simplest possible solution to every problem
- continuous redesign and rearchitecting
- automation in testing and integration
- **all the code/documentation contributions will go through the pull-request/review process**

Every 1–2 weeks, you will deliver a progress report or other evidence of your team’s efforts as required by project assignments.


## 💺 Project Phases

The project will be done in several phases, each of which will be an assignment. Phases will cover steps in the process of creating a quality software result in the context of an eXtreme Programming process model.
Assignments will be on the quality control aspects of requirements, rapid prototyping, design, coding, integration, and analysis of the building's product. 
Throughout the project, you should keep records of all evidence of your product quality control steps and evolution to make the marketing case that you have a quality result at the end of the course.

Your final products will be tested and evaluated by an independent evaluator.

## 💺 Project Schedule

The course project consists of six assignments, with separate handouts for each one.
Assignments are scheduled to be due, as indicated on the course website (preliminary, subject to change).

## 💺 Hand-In

Assignments should be all submitted through onQ, following our [git instruction](https://github.com/CISC-CMPE-327/Information/blob/master/github_basics.md).
Remember that this is a course in quality - neatness counts, and professional results are expected!


## 💺 Project Requirement

The product you are to design and build is the SeetGeek not SeatGeek online Customer-to-Customer ticket selling system.
A registered user can buy and sell tickets through this online application.
This year, we made a significant modification to the legacy design of the old project. 
This also helps us better prepare for the discussion on security issues for both native and web-based applications.

![image](https://user-images.githubusercontent.com/8474647/94135518-8ebfab80-fe31-11ea-9347-ad83f7922cf5.png)

The above control flow roughly defines the functionalities and workflows of the system. An actor is able to access his/her home directory after logged-in. 
One can also register directly through the portal. More specifications and requirements will be provided for assignment #1. 
Your team will have two options regarding the implementation:

#### Web-based real-time application with database:
The first option is to implement this as a web application, building on the top of a [template](https://github.com/CISC-CMPE-327/CI-Python).
Please follow the instructions on its README file to try it out. It should run without any problems on any platforms. 
Testing is done by controlling a browser to go through the webpages. 

![image](https://user-images.githubusercontent.com/8474647/94135588-ad25a700-fe31-11ea-8839-59699a9608db.png)

Following a typical MVC design, the frontend is a template-based server-rendering web service provided by flask.
Backend uses python data models rather than SQL language to interact with the database. 
**Backend and frontend are directly connected in a single program.**
The actors are accessing the up-to-date information in real-time. 


#### CLI-based application with file store:
The second option is the original project design in the past. It is a CLI-based application. 
The actor interacts with the system through terminal, 
and the UI testing is done by running the program with a sequence of coded user inputs. 
There is a front-end component and a backend component.
Unlike the above web application, they are two different programs and not synchronized. 
The front-end first runs during the day in different locations (such as Kingston, Toronto, and Montreal, etc), yield transaction files.
Then the backend merge the transactions and yield the new account details and available tickets for the next day.

![image](https://user-images.githubusercontent.com/8474647/94140562-689e0980-fe39-11ea-8b75-f160d6931c73.png)

If there are any conflicts (such as same ticket sold to different people, not enough balance), the backend office will simply log it and let the customer services to call and resolve issues. We also provide a GitHub testing template we created last year with pytest [here](https://github.com/CISC-CMPE-327/CI-Python/tree/python-cli-with-pytest).
