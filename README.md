#Coding Challenge
## Objective
* Create an application to manage and track performance of a school

### Criteria
* Create a relational database using a RDMS
	* Here are a few tables to keep in mind:
		* Schools
		* Admin
		* Teachers
		* Students
		* Classes
		* Topics
		* Quizzes
* Using a framework of your choosing, create an interface where:
	* As an admin:
		* I can view the performance of all my teachers (general average of quizzes for a given 		class)
	* As a teacher:
		* I can create and delete classes, topics, and quizzes
		* I can view all my classes
		* I can view all my students associated with a class
		* I can add and remove students from my class
		* I can view the performance of each student in a class
		* I can view the performance of each student given a topic of a class
	* As a student:
		* I can add and remove classes with a code provided from a teacher
		* I can view my own performance for a class
		* I can view my own performance for a topic
		* I can view my own performance for a quiz
* Set up a real-time chat system
	* Have a teacher be able to open a live lecture which students can join
	* The teacher should be able to communicate to their students and only their students through this live lecture
		* Set up socket rooms correctly, a student in one lecture should not get the messages from another lecture
* Create an API to serve up the relevant information
* Have a well thought out architecture.
	* To start, have a separte repo for your UI and your API
	* Make sure alike files are stored in the same folder, make it easier on yourself and everyone else
		* As a rule of thumb, code for the next person working on your project
* Deploy on AWS EC2

## Requirements
### Front-End
* Front load all relevant information for a user into a flux store
* Ensure you're making http requests in optimal locations
	* Best to not place http requests that make huge read operations in a component that will constantly fire off said request

### Back-End
* Cache all relevant information for a user in Redis
* Use denormalized data where necessary
	* Example: A cache column for the number of students in a cohort
* Thoughtfully craft your schemas
	* Draw them out and save a picture of it
* Secure all your routes through some authentication middleware
	* JWT, Passport, etc.
* Use Raw SQL statements no ORMs

### DevOps
* Deploy onto AWS EC2
* Secure your app with https
* Set up a proxy through nginx
* Thoughtfully craft your system design
	* Draw your system architecture and save a picture of it

### UX/UI Design
* [Model the UX/UI off of teamtreehouse](https://teamtreehouse.com/)

