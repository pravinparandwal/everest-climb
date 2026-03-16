.NET
.NET Core is a free open source, a general-purpose development platform for developing modern cloud-based software applications on Windows, Linux, and macOS operating systems. It operates across several platforms and has been revamped to make .NET fast, scalable, and modern. .NET Core is one of Microsoft’s big contributions and released under the MIT License. It offers the following features:
•	Cross-Platform
•	Open Source
•	High Performance
•	Multiple environments and development mode etc.

What are Classes and Objects?
class – Fruit 		object – Apple, Banana, Mango
class – Car		object – Volvo, BMW, scoda
So, a class is a template for objects, and an object is an instance of a class.
When the individual objects are created, they inherit all the variables and methods from the class.
The public keyword is called an access modifier
Constructors
A constructor is a special method that is used to initialize objects.

Content 1Negotiation in ASP.NET Web API
The HTTP specification (RFC 2616) defines content negotiation as "the process of selecting the best representation for a given response when there are multiple representations available." The primary mechanism for content negotiation in HTTP are these request headers:
•	Accept: Which media types are acceptable for the response, such as "application/json," "application/xml," or a custom media type such as "application/vnd.example+xml"
•	Accept-Charset: Which character sets are acceptable, such as UTF-8 or ISO 8859-1.
•	Accept-Encoding: Which content encodings are acceptable, such as gzip.
•	Accept-Language: The preferred natural language, such as "en-us".

How to Secure an ASP.NET Application using 1JWT Tokens
JSON Web Tokens (JWT) are a compact and self-contained way for securely transmitting information between parties(client <-> server) as a JSON object. 
This information can be verified and trusted because it is digitally signed. JWTs can be signed using a secret (with the HMAC algorithm) or a public/private key pair using RSA or ECDSA
A JWT (JSON Web Token) is composed of three parts: the Header, the Payload, and the Signature. Each part is Base64Url encoded and separated by dots (.).

Header:
•	The header typically consists of two parts: the type of token, which is JWT, and the signing algorithm being used, such as HMAC SHA256 or RSA.
{
  "alg": "HS256",
  "typ": "JWT"
}
Payload:
•	The payload contains the claims. Claims are statements about an entity (typically, the user) and additional data. There are three types of claims: registered, public, and private claims.
{
  "sub": "1234567890",
  "name": "John Doe",
  "admin": true
}
Signature:
•	To create the signature part, you take the encoded header, the encoded payload, a secret, the algorithm specified in the header, and sign that.
HMACSHA256(
  base64UrlEncode(header) + "." +
  base64UrlEncode(payload),
  secret)

JWT Token 1Claims in ASP.NET Core
Claims in JWT Token are used to store key data (e.g. username, timezone, or roles) in the Token payload, besides the IssuedAt (i.e. iat), which is added by default.\
In .NET Core, Claims can be used without installing any additional package, it comes from the System.Security.Claims package.

What is a 1microservices architecture?
Microservices is basically decoupling of entire application into small small services.
In a microservices architecture, a large application is split up into a set of smaller services. Each service runs in its own process and communicates with other processes by using protocols like HTTP/HTTPS, WebSocket
Each microservice must be developed autonomously and must be independently deployable.
Each microservice should own its related domain data model and domain logic.
Microservices can be based on different data storage technologies (SQL, NoSQL) and different programming languages.
•	They're small, independent, and loosely coupled.
•	Each microservice has a separate code base that a small development team can manage.
•	They're deployed independently. A team can update an existing microservice without rebuilding and redeploying the entire application.
•	They persist their data or the external state in their respective databases. Unlike in a monolithic architecture, microservices don't share databases.
What role do containers play?
Containerization is an approach to software development in which an application or service, its dependencies, and its configuration (abstracted as deployment manifest files) are packaged together as a container image.
Containers are the deployment tool that we'll use for our microservices for the rest of this module.

What is an image?
When a developer uses Docker, they create an app or service, and then they package the app or service and its dependencies in a container image. An image is a static representation of the app or service and its configuration and dependencies.
The image, when it runs, becomes the container. The container is the in-memory instance of an image. A container image is immutable

Describe the Dependency Injection
Dependency Injection is a Design Pattern that's used as a technique to achieve the Inversion of Control (IoC) between the classes and their dependencies.
ASP.NET Core comes with a built-in Dependency Injection framework that makes configured services available throughout the application. You can configure the services inside the ConfigureServices method as below.
services.AddScoped();

What happens when the main () method is declared as private?
If consider you are talking about this : public static void main(String ...args) .
suppose you have a Class as (A) and you wrote the function like : private static void main(String ...args)
Marking it as private means your class (A) doesn’t have an execution entry point, and it would be treated as a normal function written inside Class A, with name as main which takes a String array as input and don’t give any output.
Yes. You can mark the main() method as public, private or protected. If you want to initiate the entry point by any external program then you might need to make it public so it is accessible. You can mark it as private if you know there is no external usage for the application then it is better to make it private so no external application access it.
public class MainMethod
{
    private  static void Main(string[] args)
    {
        Console.WriteLine("Hello World !!");
    }
}

Why async and await Important?
They are used to handle asynchronous programming, which helps improve the performance and responsiveness of web applications.
Benefits:
1.	Non-blocking operations: async and await allow you to perform I/O-bound operations(like db calls, file reads, or web service calls) without blocking the main thread.
2.	Scalability: By not blocking threads, async and await help the application handle more concurrent requests with fewer threads, which improves scalability. This is particularly important in high-traffic web applications.

1IEnumerable will execute select query on server side, load data in-memory on client side and then filter data. IEnumerable can be used for querying data from in-memory collections like List, Array etc.

State the types of Design Patterns.
There are three types of Design Patterns-
Creational Patterns: It deals with the creation of Objects and Classes.
Structural Patterns: It deals with Class and Object Composition.
Behavioral Patterns: It deals with Class and Object Communication. 

Procedural Programing:
Procedural Programing entails writing procedures or methods that perform operations on data, whereas object-oriented programing entails creating object that contain both data and processes.

Class is a type, blue print of object.
Object is a instance of the class.
1OOPs Concept:
1.	Encapsulation
2.	Inheritance
3.	Abstraction
4.	Polymorphism

Encapsulation:
Encapsulation is the process of combining a data member and a method into a single unit.
In other words, a class It’s like holding in a capsule. That is, enclosing the related operations and data associated with an object with that particular object
Eg: School bag, our books, pens and other belongings can be stored in our school bag.  

Inheritance:	
Inheritance is the process by which one object can automatically inherits all the properties and behaviors of its parent object.
The class that inherits the member of another class is referred to as derived class(parent class), and the class whose member are inherited is referred to as the base class(child class).
Inheritance is a mechanism by which a child object acquires all the properties of the parent object. For example, suppose we are the child class, and we have access to all parent’s properties; this is the inheritance.
1.	Single – single inheritance is defined as having one base class and one derived class 
2.	Multilevel – when one class inherits another and is inherited by another, this is referred to as multilevel inheritance.
3.	Hierarchal – In which multiple classes are derived from a single base class. When a single class feature is required by multiple classes, this type of inheritance is used.
4.	Multiple – it occurs when one derived or child class accesses a property of its multiple parent or base class. 

Abstraction:
Abstraction is the process of displaying the necessary information. 
Abstraction is the process of showing only essential features of an object to the outside world while hiding the other irrelevant information, according to a proper definition.
Example: 
An example of abstraction is making coffee with coffee machine. To make coffee, you must first learn how to use your coffee machine. You must supply water and coffee beans, turn it on, and choose the type of coffee you want.

Polymorphism:
Polymorphism can be defined as the presence of multiple forms. It allow a class to have multiple implementation with the same name.
Example:
A person act as an employee at work, as a father at home, and as a customer at shopping malls.

1.	Static or compile time Polymorphism
2.	Dynamic or run time polymorphism
Static polymorphism is exemplified by method overloading. The method/function has the same name but different signature when overloading. It is also known as compile time polymorphism because the decision to call which method is made at compile time.
Late binding is another term for dynamic / runtime polymorphism. The method name and signature are used as number of parameters and parameter type must be same and may have different implementation. Dynamic polymorphism is demonstrated by method overriding.
Overloading: Method with same name and different signatures.
Overriding: Using virtual keyword and overriding in child class.

Benefits of OOPs:
1.	Encapsulation – Easier troubleshooting
2.	Inheritance – Reuse the code
3.	Abstraction – Effective problem solving
4.	Polymorphism - Flexibility

What is the role of Startup class?
Startup class is responsible for configuration related things as below.
•	It configures the services which are required by the app.
•	It defines the app's request handling pipeline as a series of middleware components.
•	But You can emit this class and Program.cs file contains all startup code.

Namespace:
The namespace keyword is used to declare a scope that contains a set of related objects. You can use a namespace to organize code elements and to create globally unique types.
The preceding example doesn't include a nested namespace.
File scoped namespaces can't include additional namespace declarations. You cannot declare a nested namespace or a second file-scoped namespace.
We can call a static method in a nested namespace
namespace HelloWorld
{
	public class Program
	{
		public static void Main(string[] args)
		{
			Console.WriteLine("Hello, World!");
		}
	}
}
namespace AnotherNamespace; // Not allowed!

What are the SOLID Principles?
SOLID Principles is an acronym of 5 principles in Object Oriented Design (OOD)
•	S - Single Responsibility Principle
•	O - Open Closed Principle
•	L - Liskov Substitution Principle
•	I - Interface Segregation Principle
•	D - Dependency Inversion Principle
Describe the Single Responsibility Principle (SRP).
In Object Oriented Programming, Single Responsibility (SRP) ensures that every module or class should be responsible for single functionality supported by the software system. In other words, every class should have one and only reason to change it.
For example, In ASP.NET MVC HomeController class should be responsible related to Home Page functionality of software system.
Describe the Open Close Principle (OCP).
Open Close Principle (OCP) states or ensures that A class, component or entity should be open for extension but close for modification. In detail, We can extend any class via Interface, Inheritance or Composition whenever it's required instead of opening a class and modifying it's code.
For example, suppose you have implemented a functionality to calculate area of Rectangle and after some time you need to calculate the area of Square, then In this case you should not modify your original class code to add extra code for square. Instead you should create one base class initially and now you should extend this base class by your square class.

Liskov Substitution Principle (LSP) states that Objects in a program can be replaced by the instances of their subtypes without modifying the correctness of a program.
In other words, if A is subtype of B then instances of B may be replaced by the instances of A without altering the program correctness.

Interface Segregation Principle (ISP) states that use many client specific interfaces instead of one general purpose interface.
In other words No client should be forced to implement other methods which it does not require. It means it's better to create a separate interface and allow your classes to implement multiple interfaces.
Explain dependency injection for controllers.
Dependency Injection is a design pattern used to inject the object dependencies inside controllers. ASP.NET core supports built-in dependency injection, just you need to register those services in the startup file inside ConfigureServices method. You can add services as constructor parameters, ASP.NET Core runtime will resolve these dependencies from the service container.
You can perform dependency injection in two ways.
•	Constructor Injection
•	Action Injection using FromServices attribute.
•	You can access additional settings by using options pattern instead of directly injecting I Configuration inside the controller.


Microsoft Azure
Data member property?
Private constructor?
Singleton design pattern?
How to handle exception?
Throw difference, new and define exception?
Major advantage using .ner core?
Dependency injection? few redimade ?
Have you used middleware?
Difference middleware and filters? Where can we use both?
Generic class, interface, method? Generic and non-generic collection?
Content negotiator?
Handle cors?


git stash
This command can be used when we want to save our work without staging or committing the code to our Git repository and want to switch between branches.
git stash -u
This command is used when we want to stash the untracked files.
git stash pop
This command is used when we are back on our branch and want to retrieve the code.
git revert [commit id]
The git revert command can be considered as an ‘undo’ command. However, it does not work as the traditional ‘undo’ operation. It figures out how to invert the changes introduced by the commit and appends a new commit with the resulting inverse content.
git diff [commit-id-of-version-x] [commit-id-of-version-y]
The git diff command is often used along with the git status and git log commands to analyze the current state of our Git repository. We use git log to get the details of commit IDs.
git merge [another-file-name] => git merge branch1
git merge is used to combine two branches. Eg. If you are on feature branch and want to merge main branch code which recently someone has updated that time you can use rebase command.
git rebase [base] => git rebase master
Rebase is the process of moving and combining a sequence of commits to a new base commit. Rebasing is changing the base of our branch from one commit to another, making it appear as if we’ve created our branch from a different commit.
git fetch
When we use the command git fetch, Git gathers any commit from the target branch that does not exist in our current branch and stores it in our local repository. However, it does not merge it with our current branch.
git reset –hard [SOME-COMMIT]
We use this command to return the entire working tree to the last committed state.

Git cherry pick
Cherry picking is the act of picking a commit from a branch and applying it to another. git cherry-pick can be useful for undoing changes. For example, say a commit is accidently made to the wrong branch. You can switch to the correct branch and cherry-pick the commit to where it should belong.
git cherry-pick 


Explain the difference between rebasing and merge in Git?


Introduce yourself
Hello, myself Pravin Kashinath Parandwal, I’m dedicated software developer with over 10 years of experience in the industry. I am a fullstack developer using ReactJS, Node.js, Angular, JavaScript, HTML, CSS,SCSS, TailwindCSS, Bootstrap and databases like MySQL, SQL, MongoDB which helps me to integrate front-end and back-end systems effectively.
I have worked with various tools such as JIRA, GIT, GitHub, Bitbucket, Postman, Swagger, VS Code, key-cloak, Workbench, AWS and CI/CD pipeline. 
My experience spans across diverse domains, including Healthcare, Banking, Airline, Media, and CRM. In my last project, I worked on a healthcare application. It had several modules to manage instrument data. I was mainly responsible for the core cloud application, which was the main system where all other modules connected. This application helped users to see visual data for analysis and reports. There were different types of users, such as cloud customers, on-premise customers, hybrid customers, and clients. Each user had their own dashboard to analyze data and use features like adding, updating, and deleting records. They could also view, upload, and download documents, and work with tables that had filters and reports.
I’m currently pursuing an MBA and was recently recognized as the “Annual - Most Valuable Developer”. As a senior engineering leader, I had the opportunity to lead and mentor a team of developers. My leadership involved guiding the team through the development lifecycle, promoting coding best practices, and creating a collaborative environment because I believe that the best ideas develop from teamwork.
I look forward to contributing my skills and knowledge to create innovative and impactful solutions.
Thank you for considering my profile.


How you have 60 days Notic period?
I was working on an important project for the past few months, and that has ended for now. So, I don’t have a lot on my plate now. My manager and HR are flexible and can release me within the next 60 days. This is a good time for me to explore new opportunities.

 Over the past few months, I was engaged in an important project, which has now been completed. At the moment, I don’t have a lot on my plate, and my manager and HR both are flexible to release me within the next 60 days.
I wanted to share that I am currently exploring onshore opportunities, and I feel this is an appropriate time to do so.


Notes – 
I’ve been actively exploring onsite job opportunities and would greatly appreciate your support in connecting me with relevant people who could assist or guide me in this process.
 
Profile Summary:
I am a Full Stack Software Developer with 10+ years of experience, specializing in ReactJS, Node.JS (MERN stack), and Angular. I have been working with Persistent Systems for the past 5+ years.
 
Primary Skills:
•	Frontend: Angular, ReactJS
•	Backend: Node.JS
•	Databases: MySQL, SQL, MongoDB
•	Environments: AWS, CI/CD Pipeline
Key Highlights:
•	Certified in GenAI Foundation, GenAI Practitioners, and AI Prompt Engineering
•	Completed Lead, Motivate, Engage People certification
•	Recipient of the Annual Award – “Most Valuable Player in Developer”
•	Currently pursuing an MBA from Manipal University
•	Recognized in PULSE as a “Performance Execution Lead”
I’d be grateful if you could review my profile and share any feedback or suggestions.
Looking forward to hearing from you. Thank you for your time and consideration.


Team Lead speech
(Seeking an opportunity to leverage my technical expertise and passion for innovation while developing leadership skills in dynamic environment.)
I have collaborated with team members to optimize code efficiency and part of discussion with product manager, UX designers, and QA teams to ensure alignment of development efforts with overall project goals.
Do you see a possibility for an international assignment for me? If there is a business need, I would be very happy to go.

Send mail content.
I am very fascinating in applying for the UI Developer position.
Please take a moment to review my attached Application Document.
It would be a sincere pleasure to hear back from you soon to discuss this exciting opportunity.

Last Project: 
It was bank domain project. It had different modules to manage credit cards data. I was working on B2B credit card collection application. 
Basically Credit card collection data is allocated to Agencies and then individual agency allocate case to the agent, and set target collection amount. Then agent works on his data and update in the application. 
B2B application has different user roles likes agency, agent, agency admin, call processor agent, each role has different menus, different functionalities such as add/update/delete functionality, document view/download/upload and different reports, table, filters etc.

Introduction:
Hello, myself Pravin Kashinath Parandwal, I’m dedicated software developer with over 8.9 years of experience in the industry. My journey in software development has been both challenging and rewarding, allowing me to grow my skills and knowledge across various domains and technologies. 
Professional experience:
In my career, I have primarily focused on UI development using Angular, JavaScript, HTML, CSS, SCSS, Bootstrap. My role as UI developer involved creating dynamic, responsive, and user-friendly interfaces that enhance the user experience.
While my primary expertise lies in UI development, I also have a basic understanding of backend technologies such as .NET, spring boot, MySQL, SQL. This knowledge has enabled me to collaborate effectively with backend developer, understand the full-stack development process, and contribute to the overall success of projects.
Tools and technologies:
Throughout my career, I have worked with various tools to enhance productivity and streamline the development process. JIRA has been an essential tool for project management and issue tracking. VS Code, Visual Studio, SQL Server Management Studio has been my preferred tools, offering a rich set of features and extensions that enhance coding efficiency. GIT, GitHub, GitLab, Bitbucket has facilitated version control, enabling smooth collaboration with team members and maintaining code quality.
My experience extends to project development, where I have worked with AWS in windows and c-Panel in Linux environments. Deploying projects on AWS has provided me with valuable insights into cloud computing, scalability, and performance optimization. 
Leadership and mentoring:
As a senior engineering lead, I had the privilege of leading and mentoring a team of talented developers. My leadership involved guiding the team through the development lifecycle, ensuring adherence to best practices, fostering a collaborative and innovative work environment, encouraging team members to take ownership of their tasks and support them in achieving their professional goals. And I believe, the best ideas are developed in team.
Domain experience:
My experience spans across diverse domains, including Banking, Airline, Media, and Customer Relationship Management. Each domain has presented unique challenges and opportunities, allowing me to develop a comprehensive understanding of industry-specific requirements and best practices.
Last Project: 
It was bank domain project. It had different modules to manage credit cards data. I was working on B2B credit card collection application. 
Basically, Credit card collection data is allocated to Agencies and then individual agency allocate case to the agent and set target collection amount. Then agent works on his data and update in the application. 
B2B application has different user roles likes agency, agent, agency admin, call processor agent, each role has different menus, different functionalities such as add/update/delete functionality, document view/download/upload and different reports, table, filters etc.
Learning:
I am a firm believer in continuous learning and professional development. I have actively participated in internal learning sessions. Also I have completed GenAI courses, where I have gained insights into emerging technologies, industry trends, and advance development techniques. There courses have not only expanded my knowledge but also inspired me to explore new areas and stay ahead of the curve.
Community Involvement:
Beyond my professional endeavors, I am actively involved in social events and community initiatives. I have participated in river cleaning drives, where we work together to preserve our natural resources and promote environmental sustainability. Additionally, I have been part of tree plantation campaigns, contributing to greener and healthier surroundings.
Conclusion:
I am excited about the opportunities that lie ahead and look forward to contributing my skills and knowledge to create innovative and impactful solutions.
Thank you for considering my profile.


I hope this message finds you well. I'm reaching out because I noticed you work at Persistent Systems, and I'm very interested in the UI Developer position currently open at Persistent Systems.
I would be grateful if you could refer me for this role or connect me with the hiring team.
A bit about my background: I have around 1.5 years of experience at Parallel Minds, where I've built frontend applications with ReactJS/NextJS, TypeScript/JavaScript.
I believe my experience aligns well with this opportunity, and I'm confident I can contribute meaningfully to your team.
My resume is attached for your reference. I'd be happy to provide any additional information or discuss my qualifications further.
Thank you for considering my request!


II. Summary Introduction:
Hello, myself Pravin Kashinath Parandwal, I’m dedicated software developer with over 8.9 years of experience in the industry. I have primarily focused on UI development using Angular, JavaScript, HTML, CSS, SCSS, Bootstrap etc. Along with my UI skills, I also have a basic understanding of backend technologies such as .NET, MySQL, SQL, which helps me to integrate front-end and back-end systems effectively.
I have worked with various tools such as JIRA, GIT, GitHub, Bitbucket, Postman, Swagger, VS Code, Visual Studio, SQL Server Management Studio, Workbench, AWS etc. Recently, I awarded as a “Most Valuable Player in Developer” in this Annual Award 2024.
My experience spans across diverse domains, including Banking, Airline, Media, and CRM. In last project I was working on bank application. It had different modules to manage credit cards data. I was working on B2B credit card collection application. Basically, Credit card collection data is allocated to Agencies. Those agencies allocate that credit card data to the agents with certain criteria. Then individual agents work on that data and updates it in the application. B2B application has different user roles likes agency, agency admin, agent, call processor agent, etc. Each role has different menus, functionalities such as add/update/delete, document view/download/upload and different table with filters and reports etc.
As a senior engineering lead, I had the privilege of leading and mentoring a team of developers. My leadership involved guiding the team through the development lifecycle, promoting best practices, and fostering a collaborative environment because I believe that the best ideas emerge from teamwork.
I look forward to contributing my skills and knowledge to create innovative and impactful solutions.
Thank you for considering my profile.

SQL
What is a database?
A database is a systematically organized collection of data arranged into tables composed of rows and columns. The primary purpose of databases is to efficiently store, manage, and retrieve data.

What is SQL?
SQL means Structured Query Language and is used to communicate with relational databases. It proposes a standardized way to interact with databases, allowing users to perform various operations on the data, including retrieval, insertion, updating, and deletion.

What are the different types of SQL commands?
•	SELECT: Retrieves data from a database.
•	INSERT: Adds new records to a table.
•	UPDATE: Modifies existing records in a table.
•	DELETE: Removes records from a table.
•	CREATE: Creates a new database, table, or view.
•	ALTER: Modifies the existing database object structure.
•	DROP: Deletes an existing database object.

What is a primary key in SQL?
It is a unique identifier for each record in a table. 
It ensures that each row in the table has a distinct and non-null value in the primary key column. Primary keys enforce data integrity and create relationships between tables.

What is indexing in SQL?
Indexing is the way to get an unordered table into an order that will maximize the query’s efficiency while searching.
Indexes in SQL are specialized lookup tables that are used by the database search engine to accelerate data retrieval. 

PostgreSQL
7.	How do you optimize queries in PostgreSQL?
o	Use indexes.
o	Avoid SELECT *.
o	Use EXPLAIN to analyze queries.
o	Normalize data properly.

What is Normalization in a Database?
Normalization means arranging data in a database so there is no duplicate data and everything stays consistent and easy to maintain.

What is a 1foreign key?
That is this field points to the primary key of another table. 
This usually creates a kind of link between the two tables. 
A Foreign key is a field that can uniquely identify each row in another table. 
And this constraint is used to specify a field as a Foreign key.
CREATE TABLE Orders
(
O_ID int NOT NULL,
ORDER_NO int NOT NULL,
C_ID int,
PRIMARY KEY (O_ID),
FOREIGN KEY (C_ID) REFERENCES Customers(C_ID)
)

How to find duplicate records?
select *, COUNT(ID) as DuplicateSalary from Customers group by SALARY having count(SALARY) >1;
select *, COUNT(ID) as DuplicateSalary from Customers group by SALARY;
select col1, col2, count(*) AS count from your_table GROUP BY col1, col2 HAVING COUNT(*) >1;


How to find second highest salary?
select * from Customers order by SALARY DESC LIMIT 1 OFFSET 1;
select max(SALARY) from Customers where SALARY NOT IN(select max(SALARY) from Customers);

Define a 1Unique Key in SQL.
Often referred to as a unique constraint, a unique key guarantees that every value in a column (or a combination of columns) remains distinct and cannot be replicated within a table. 
In contrast to a primary key, a table has the flexibility to incorporate multiple unique keys.

What is the difference between primary key and unique constraints? 
The primary key cannot have NULL values, the unique constraints can have NULL values. There is only one primary key in a table, but there can be multiple unique constraints. The primary key creates the clustered index automatically but the unique key does not.

Explain the difference between DELETE and TRUNCATE commands.
The DELETE command is used by professionals to remove particular rows from a table based on a condition, allowing you to selectively delete records. 
TRUNCATE, on the other hand, removes all rows from a table without specifying conditions. TRUNCATE is faster and uses fewer system resources than DELETE but does not log individual row deletions.

What is a JOIN in SQL, and what are its types?
A JOIN operation merges information from two or more tables by utilizing a common column that links them together. 
Various types of JOINs exist, like INNER JOIN, LEFT JOIN, RIGHT JOIN, and FULL JOIN. 
These JOIN variations dictate the manner in which data from the involved tables is paired and retrieved.
Explain different types of joins with examples.
•	INNER JOIN: Gathers rows that have matching values in both tables.
•	RIGHT JOIN: Gathers all rows from the right table and any matching rows from the left table.
•	LEFT JOIN: Gathers all rows from the left table and any matching rows from the right table.
•	FULL JOIN: Gathers all rows when there's a match in either table, including unmatched rows from both tables.
Example:
SELECT employees.name, departments.name
FROM employees
LEFT JOIN departments ON employees.department_id = departments.id;

What is the difference between INNER JOIN and LEFT JOIN?
o	INNER JOIN returns matching rows from both tables.
o	LEFT JOIN returns all rows from the left table, even if there's no match in the right.

What is the difference between INNER JOIN and OUTER JOIN?
INNER JOIN: Returns only matching records from both tables.
LEFT OUTER JOIN: Returns all records from left table, and matching records from the right table. If no match, NULL is returned.
RIGHT OUTER JOIN: Returns all records from the right table, and matching records from the left.
FULL OUTER JOIN: Returns all records from both table, matching where possible
Key Difference:
•	Intersection (matched data only)
•	Union + NULLs (matched + unmatched data)

What do you mean by a NULL value in SQL?
A NULL value in SQL represents the absence of data in a column. It is not the same as an empty string or zero; it signifies that the data is missing or unknown. NULL values can be used in columns with optional data or when the actual data is unavailable.

Explain the differences between SQL and NoSQL databases.
SQL databases are characterized by their use of structured tables and strict adherence to a predefined schema, making them ideal for managing structured data with a strong focus on data consistency and transaction support. 
In contrast, NoSQL databases are non-relational and excel in handling unstructured or semi-structured data, frequently employed for scalable, distributed, and adaptable data storage solutions.

What is a table and a field in SQL?
In SQL, a table is a structured data collection organized into rows and columns. 
Each column in a table is called a field, representing a specific attribute or property of the data.

What is a constraint in SQL? Name a few.
A constraint in SQL defines rules or restrictions that apply to data in a table, ensuring data integrity. Common constraints include:
•	PRIMARY KEY: Ensures the values’ uniqueness in a column.
•	FOREIGN KEY: Enforces referential integrity between tables.
•	UNIQUE: Ensures the uniqueness of values in a column.
•	CHECK: Defines a condition that data must meet to be inserted or updated.
•	NOT NULL: Ensures that there are no NULL values in a column.

What are indexes in SQL?
Indexes improve the data retrieval operations speed. 
They provide a quick way to locate specific rows in a table by creating a sorted data structure based on one or more columns. 
Indexes are essential for optimizing query performance.

Explain GROUP BY in SQL.
The GROUP BY clause organizes rows from a table into groups based on the values in one or more columns. 
It is commonly employed alongside aggregate functions like SUM, COUNT, AVG, MIN, and MAX to perform computations on data that has been grouped together.

What is an SQL alias?
An SQL alias serves as a transitory label bestowed upon either a table or a column within a query, with the primary purpose of enhancing the clarity of query outcomes or simplifying the process of renaming columns for improved referencing. 
For example:
SELECT first_name AS "First Name", last_name AS "Last Name" FROM employees;

Describe the difference between WHERE and HAVING in SQL.
The WHERE clause is employed to restrict individual rows before they are grouped, such as when filtering rows prior to a GROUP BY operation. Conversely, the HAVING clause is utilized to filter groups of rows after they have been grouped, like filtering groups based on aggregate values.

What is a stored procedure?
A SQL stored procedure comprises precompiled SQL statements that can be executed together as a unified entity. 
These procedures are commonly used to encapsulate business logic, improve performance, and ensure consistent data manipulation practices.

What are aggregate functions? Can you name a few?
Aggregate functions in SQL perform calculations on a set of values and return a single result.
•	SUM: To calculate the sum of values in a column.
•	COUNT: To count a column's number of rows or non-null values.
•	AVG: To calculate the average of values in a column.
•	MIN: To retrieve the minimum value in a column.
•	MAX: To retrieve the maximum value in a column.

What is a subquery? Provide an example.
A subquery refers to a query that is embedded within another query, serving the purpose of fetching information that will subsequently be employed as a condition or value within the encompassing outer query. For example, to find employees with salaries greater than the average salary:
SELECT name
FROM employees
WHERE salary > (SELECT AVG(salary) FROM employees);


Which is faster, subquery or join?
JOINs are generally faster than subqueries, especially for large datasets. Subqueries can be more complex and harder to read, especially when there are multiple levels of nesting. JOINs can be easier to read and understand, especially for simple queries

What is the difference between UNION and UNION ALL?
UNION merges the outcomes of two or more SELECT statements, removing duplicate rows, whereas UNION ALL merges the results without removing duplicates. 
While UNION ALL is faster, it may include duplicate rows.

How do you implement error handling in SQL?
Error handling in SQL is typically achieved using try-catch blocks (in SQL Server) or EXCEPTION blocks (in Oracle). These blocks allow you to handle and log errors gracefully to prevent application crashes.

What is a transaction in SQL?
A transaction in SQL is a sequence of one or more SQL operations treated as a single unit of work. Transactions ensure that database operations are either completed successfully or rolled back entirely in case of failure.

Describe the data types in SQL.
SQL supports various data types, including numeric, character, date/time, and binary types. Common data types include INT, VARCHAR, DATE, and BLOB, among others. Data types define the kind of values a column can hold.

How do you create a 1stored procedure?
You use the CREATE PROCEDURE statement to create a stored procedure in SQL. A stored procedure can contain SQL statements, parameters, and variables. Here's a simple example:
CREATE PROCEDURE GetEmployeeByID(@EmployeeID INT)
AS
BEGIN
   SELECT * FROM employees WHERE employee_id = @EmployeeID;
END;

How do you manage large-scale databases for performance?
Managing large-scale databases for performance involves various strategies, including proper indexing, partitioning, query optimization, hardware optimization, and caching. 
Monitoring and fine-tuning the database is crucial to ensure optimal performance as data volumes grow.

Explain the concept of table partitioning.
Partitioning a table involves the strategy of breaking down a sizable table into smaller, more easily handled segments known as partitions. 
This method can enhance query efficiency by permitting SQL Server to focus solely on pertinent partitions while executing queries. 
Typically, partitioning is carried out using a column characterized by a high cardinality, such as date or region.

Discuss the strategies for database backup and recovery.
Ensuring data availability and disaster recovery relies on the implementation of vital backup and recovery strategies. These strategies encompass various methods, such as full backups, differential backups, transaction log backups, and regular testing of restoration procedures.

What is the difference between CHAR and VARCHAR2 datatype in SQL? 
Both of these data types are used for characters, but varchar2 is used for character strings of variable length, whereas char is used for character strings of fixed length. 
For example, if we specify the type as char(5) then we will not be allowed to store a string of any other length in this variable, but if we specify the type of this variable as varchar2(5) then we will be allowed to store strings of variable length. We can store a string of length 3 or 4 or 2 in this variable.

What do you mean by data definition language? 
Data definition language or DDL allows to execution of queries like CREATE, DROP, and ALTER. That is those queries that define the data.
What do you mean by data manipulation language?
Data manipulation Language or DML is used to access or manipulate data in the database. It allows us to perform the below-listed functions: 
•	Insert data or rows in a database
•	Delete data from the database
•	Retrieve or fetch data
•	Update data in a database.

What is a trigger?
The trigger is a statement that a system executes automatically when there is any modification to the database. In a trigger, we first specify when the trigger is to be executed and then the action to be performed when the trigger executes. Triggers are used to specify certain integrity constraints and referential constraints that cannot be specified using the constraint mechanism of SQL.

What is SQL 1View
A view in SQL is a virtual table that is stored in the database with an associated name.
A view can contain rows from an existing table.
The data in the view does not exist in the database physically.
CREATE VIEW CUSTOMERS_VIEW AS SELECT * FROM CUSTOMERS;
SELECT * FROM CUSTOMERS_VIEW;
DROP VIEW CUSTOMERS_VIEW;

Delete and truncate difference?
Candidate key?
Non-clustored and cluctered key? Which key will get you(primary or unique)


PostgreSQL
7) What is a stored procedure and when do you use it?
Answer:
A stored procedure is a saved SQL function that runs on the database. I use it for complex logic that needs to run close to the data, like batch updates or validations.
8) How do you handle schema changes in production?
Answer:
I use migration tools like Knex or Sequelize. I test changes in staging, apply them during low-traffic hours, and always take backups before applying.
9) What is a foreign key and why is it important?
Answer:
A foreign key links one table to another. It keeps data consistent and prevents orphan records.
PostgreSQL — Scenario Q&A
7) Scenario: A report query takes 15 seconds and locks tables.
Question: How do you optimize?
Answer:
•	Run EXPLAIN ANALYZE to see slow operations.
•	Add indexes on filter/sort columns; consider partial indexes.
•	Replace SELECT * with needed columns only.
•	Precompute aggregates into a materialized view or nightly batch.
•	Use read replicas for reporting.
•	Paginate results to avoid full scans


Who Is a Team Leader?
•	A team leader leads or manages a group of employees by providing guidance, focus, motivation, and instruction. 
•	The team leader is a mid-to-senior level job role in an organization. 
•	Their primary duties are setting team workloads, assessing employee performance, communicating goals and deadlines, and encouraging team members to do their best. 
•	A team leader is responsible for managing, guiding, organizing, and planning for the team and helping to resolve any conflict that can arise within the group.
•	When hiring a team leader, employers look for excellent leadership skills, good communication skills, approachability, conflict management, and resolution skills. 
•	A strong sense of integrity and the ability to innovate and inspire are also preferred in candidates aspiring to become team leaders.

Team Leader Qualities
Most team leadership positions require qualities like:
•	Excellent Verbal and Non-verbal Communication Skills – clear and effective communication can help a team leader to lead the team efficiently towards accomplishing their goals and to communicate clearly with both team and supervisor.  
•	Organizational Skills – good organizational abilities are essential to keep directions, roles and expectations clear and organized in a team setting. 
•	Delegating and Motivating Abilities – the team leader must have the ability to delegate tasks to team members based on each of their talents and capabilities. This makes team members feel motivated and confident of their abilities.
•	Integrity – team leaders should lead by example in order to establish mutual respect and appreciation between them and their team members. 
•	Confident Work Ethics – by demonstrating a confident work ethic with great expectations and consistent results, a team leader can instill the same confidence and expectations among team members, thus ensuring greater focus and productivity. 

What are the most important values you demonstrate as a team leader?
I think my dedication, integrity, commitment and courage are my most important values. 
I try to stay honest and trustworthy in all my actions to establish credibility as a leader. 
By working with this conviction, I’m able to build stronger relationships with team members and guide them to higher levels of performance. 

How do you gain commitment from your team?
I influence and persuade my team to set specific objectives and accept the project idea. 
Once they start cooperating and working as a cohesive unit, they are on board to accomplish the goal. 

How would you resolve a dispute between two team members?
I feel that a dispute can not only affect the individuals, but the overall team and the project as well.
I listen to both sides of the argument and carefully consider their feedback before coming to a decision that would put the team in the best position for success. 
I’d explain why we are choosing the solution to resolve the situation effectively.  

What is the difference between a team leader and a team manager?
A team leader inspires and motivates team members to achieve their goals, while a team manager handles tasks and responsibilities of the team and makes sure that others get their work done. 

How can a team leader fail?
A team leader can fail if they cannot get their team on board to accomplish the goals of the organization. External factors like lack of resources, time constraints - though in the leader’s control - can also contribute to their failure. 

What is your greatest strength?
I believe I can lead and inspire a team to perform their best and try to accomplish goals. I can achieve this through relationship building, being motivated about the goals, and influencing others around me. 

What is your greatest weakness?
Sometimes I must delegate tasks to others that I know I can do better. But if I do not delegate, I could end up with my hands too full of work to handle myself. 
I have learnt time management strategies to figure out how to effectively manage tasks to overcome this weakness.

How do you get others to accept your ideas?
I try to explain about the benefits of the idea and how to use it. 
I stay open to discussions and other thoughts and can even tweak my ideas in a way that we can all agree. 
When you gain acceptance from others, you are much more successful in accomplishing the goals than when you make it compulsory to follow an idea.

How do you motivate your team?
I try to figure out what motivates my individual team members, so I can individually speak to them about how a goal or change can benefit them. 
I make sure that I give enough positive and constructive feedback to help them perform effectively. 
I always stay true to my words, so when I speak with conviction, my team is on board with giving it their best. 

How do you lead through change?
As a leader, I have to be the first one to accept change so I can motivate others to follow. 
I communicate the change to my team with the conviction that it’s the right path to embrace.  I try to answer any concern that they may have or find resources to answer them. 
I hear out their apprehensions and help them through the transition.

When do you consider success for you as a leader?
I measure success in terms of the goals that the team achieves. If a team member is successful, then it indicates success for my leadership.

What is the most difficult part of being a leader?
Being a team leader, you can feel alone in some ways in spite of being part of a team. 
The leader’s responsibility is to see the end goal and objectives of an organization and guide others towards it. When others are not on the same track, the leader has to be the only one to ensure they’re back on board.

What qualities should a team leader have?
Here are some important qualities that a team leader should have:
•	Acknowledgment, appreciation and giving due credit 
•	Active listening
•	Showing commitment
•	Having a clear vision
•	Investing in the team's future
•	Acting with integrity
•	Acting objectively
•	Motivating others

Describe a time when you faced a significant challenge in a project. How did you handle it?
Tell me about a time when you had a disagreement with a team member. How did you resolve it?
Describe a situation where you had to meet a tight deadline. What steps did you take to ensure you met it?
Have you ever had to deal with a difficult stakeholder or client? How did you handle the situation?

Give an example of how you ensured quality in your code.
To ensure quality, I followed best practices like writing unit tests, performing code reviews, and adhering to coding standards.

What is Agile Methodology?
Agile is a way of building software step by step. Instead of doing everything at once, we work in small parts, deliver quickly, make changes when needed, and keep everyone working together
Mention key principles:
•	Short development cycles (sprints)
•	Continuous feedback and improvement
•	Transparency and communication
•	Prioritization based on business value
Give an example from your experience: 
In my previous role, we implemented Scrum within the Agile framework. We worked in 2-week sprints and conducted daily stand-up meetings to ensure alignment. At the start of each sprint, we held sprint planning sessions to define priorities and goals. At the end of the sprint, we conducted sprint retrospectives to discuss what went well, what could be improved, and what practices to continue. We used Jira to manage and track all these processes. This approach helped us shorten release cycles and respond quickly to customer feedback

Highlight benefits:
•	Faster delivery
•	Better quality through continuous testing
•	Improved customer satisfaction

What are the types of testing in react and nodejs?
Unit Testing – Test small pieces like functions or components in isolation. 
Integration Testing – Check if components work together (e.g., component + API). 
End-to-End (E2E) Testing – Test the full user flow in the browser. 
API Testing – Validate REST/GraphQL endpoints (status codes, responses).
Performance & Security Testing – Check speed and vulnerabilities.
Sanity Testing - Quick checks to confirm core flows work after deploy.
In React, we do unit tests for components, integration tests for combined parts, and E2E tests for full user flows using tools like Jest, React Testing Library, and Cypress. In Node.js, we test individual functions, APIs, and integrations using Jest, Mocha, and Supertest. This ensures both frontend and backend work correctly together

Q1: As a Senior Engineering Lead working on Node.js and React.js, what standard processes do you follow in your projects?
Answer:
In my projects, I ensure we follow industry best practices and Agile methodology.
•	For Node.js, we maintain a modular code structure, follow REST/GraphQL API standards, implement proper error handling, logging, and use tools like ESLint and Prettier for code consistency.
•	For React.js, we follow component-based architecture, apply reusable hooks, maintain state management with Redux/Context, and ensure optimized rendering.
•	We use Git branching strategy (feature branches, pull requests, code reviews) and CI/CD pipelines for automated builds and deployments.
•	Testing is a key part of our process, so we implement unit tests (Jest, Mocha) and integration tests to ensure reliability.

What are the difference between REST API and RESTfull API?
A REST API uses REST principles but may not follow all rules. A RESTful API strictly follows REST constraints like statelessness, uniform resource naming, and cacheability. So, all RESTful APIs are REST APIs, but not all REST APIs are fully RESTful.

What are differences between REST API and graphQL API?
REST API
•	Structure: Uses multiple endpoints (e.g., /users, /posts).
•	Data Fetching: Fixed response structure; you often get more or less data than needed.
•	Over-fetching / Under-fetching: Common problem because endpoints return predefined fields.
•	Versioning: Usually requires versioning (e.g., /v1/users) when API changes.
•	HTTP Methods: Uses GET, POST, PUT, DELETE for CRUD operations.
GraphQL API
•	Structure: Single endpoint for all queries (usually /graphql).
•	Data Fetching: Client specifies exactly what data it needs in a query.
•	No Over-fetching / Under-fetching: You get only the requested fields.
•	Versioning: No need for versioning; schema evolves without breaking clients.
•	Flexibility: Supports complex queries and nested data in one request.

REST uses multiple endpoints with fixed responses, which can lead to over-fetching or under-fetching data. GraphQL uses a single endpoint and lets the client ask for exactly what it needs, reducing unnecessary data transfer and making APIs more flexible.

Q2: What is your approach towards work and collaboration with your team members?
Answer:
My approach is collaborative and supportive. I believe in leading by example — writing clean, maintainable code, and encouraging best practices. With team members:
•	I mentor juniors by guiding them on problem-solving rather than just giving direct solutions.
•	I promote knowledge sharing sessions to keep the team updated on new tech (like React 18 features or Node.js performance improvements).
•	I make sure everyone feels ownership of the project by involving them in design and decision-making.
•	I encourage open communication and follow a “fail-fast, learn-fast” mindset, so issues are discussed early.
This approach keeps the team motivated, improves code quality, and creates a positive work culture.

Q2: How do you balance coding responsibilities with leadership tasks?
Answer:
I dedicate around 40-45% of my time to leadership activities like design reviews, mentoring, sprint planning, and stakeholder communication. The rest of the time, I remain hands-on with coding — usually working on complex or critical modules. This balance allows me to stay technically sharp while ensuring the team has guidance and support.
Q2: Why did you choose Node.js for microservices architecture?
Answer:
Node.js is event-driven, lightweight, and handles concurrent requests efficiently, which is ideal for microservices.
•	Fast I/O operations make it great for APIs.
•	Huge ecosystem (NPM packages) reduces development time.
•	Works well with containerization (Docker) and cloud platforms (AWS, GCP, Azure).
•	Easy to integrate with React.js frontend since both use JavaScript, ensuring full-stack consistency.

Git
11.	What is the difference between git merge and git rebase?
•	merge combines branches and keeps history.
•	rebase rewrites history to make it linear.
12.	How do you resolve merge conflicts?
•	Git shows conflicting files.
•	Manually edit the files.
•	Add and commit the resolved changes.
Sprint Planning
15.	How do you plan a sprint?
•	Review backlog.
•	Estimate tasks (story points).
•	Set sprint goals.
•	Assign tasks based on team capacity.
16.	How do you handle scope changes during a sprint?
•	Discuss with the team and product owner.
•	Re-prioritize if needed.
•	Avoid frequent changes to maintain focus.

What is your experience with CI/CD pipelines?
Answer:
I have built and maintained CI/CD pipelines using tools like Jenkins, GitLab CI/CD, and GitHub Actions.
•	The CI part ensures code quality: linting, unit tests, integration tests, and build verification.
•	The CD part deploys artifacts to AWS services (EC2, S3, Lambda).
For example, in one project, every commit triggered build/test pipelines, and on merge to main, an automatic deployment happened to a staging environment. Production deployments required approval for safety.
Q5: How do you use S3 in your projects?
Answer:
I’ve used S3 buckets mainly for:
•	Hosting static React apps (npm run build → upload to S3 → enable static website hosting).
•	Storing user-uploaded files (images, documents).
•	Versioning files for rollback.
•	For secure access, I use pre-signed URLs so that clients can directly upload/download files without exposing credentials.

How do you make an S3 bucket secure?
Answer:
•	Block public access by default and use IAM roles/policies for controlled access.
•	Enable encryption (AES-256/SSE-KMS) for data at rest.
•	Use HTTPS (SSL/TLS) for data in transit.
•	Enable bucket versioning and logging for audit trails.

What is the role of a Data Handling Platform (DHP) in your project?
Answer: In my project, the DHP Layer acted as a middleware/data hub that connected frontend applications with backend systems. It handled data validation, business rules, and routing of requests to microservices and external APIs. This separation made the system more scalable, secure, and easier to maintain.

Why did your team decide to implement a DHP layer instead of direct API calls?
Answer:
Direct API calls would have tightly coupled the frontend with backend systems, making the application harder to scale and maintain. The DHP provided:
•	Abstraction of backend complexity.
•	Reusability of business logic across multiple frontends.
•	Security enforcement (authentication, authorization, rate-limiting).
•	Data consistency across different services.
This made the architecture scalable, flexible, and maintainable.



AWS Cloud
How do you monitor a Node.js app on AWS?
Answer:
I use CloudWatch for logs and metrics, set alarms for errors or high CPU, and use X-Ray for tracing requests across services.
11) What is the difference between EC2 and Lambda?
Answer:
EC2 is a virtual server where you manage everything. Lambda is serverless, you just run code without managing servers. Lambda is good for short tasks; EC2 is better for long-running apps.
12) How do you set up auto-scaling in AWS?
Answer:
I use Auto Scaling Groups with EC2. I set rules based on CPU or request count. AWS adds or removes instances automatically.

9.	What services have you used in AWS? Common ones: EC2 (servers), S3 (storage), RDS (databases), Lambda (serverless), CloudWatch (monitoring), IAM (security).
10.	How do you secure an AWS application?
•	Use IAM roles and policies.
•	Enable encryption (S3, RDS).
•	Use security groups and VPCs.
•	Rotate access keys regularly.

Behavioral & Leadership
1) Tell me about a complex project you led.
Answer:
I led a multi-service web platform with React (frontend), Node.js (backend), and PostgreSQL. We split features into microservices, set up CI/CD with GitHub Actions, and used AWS (EC2, S3, RDS). I focused on clear requirements, small deliverables, automated tests, and weekly demos. Result: 30% faster delivery and fewer production issues.
2) How do you handle production incidents?
Answer:
I set up alerts (CloudWatch), check logs first, roll back if needed, and triage the root cause. Then I add a test to prevent it in future, write a short postmortem, and improve monitoring.
3) How do you mentor juniors?
Answer:
Pair programming, code reviews with specific feedback, share examples, small learning tasks, and weekly check-ins.
4) How do you manage scope creep?
Answer:
Freeze scope after sprint planning. For urgent changes, we re-prioritize, swap tasks of similar size, and document why.
5) How do you ensure quality?
Answer:
Clear acceptance criteria, linting, unit/integration tests, code reviews, performance checks, and feature flags.

CI/CD Pipeline
36) What is CI/CD?
Answer:
Continuous Integration (CI)
Developers frequently merge code changes into a shared repository.
Each change triggers automated builds and tests to catch issues early.
Goal: Ensure code is always in a working state.
Continuous Delivery (CD)
After CI, the code is automatically prepared for deployment to staging or production.
Goal: Make releases fast, safe, and repeatable.
Continuous Deployment (CD) (extended)
Every change that passes tests is automatically deployed to production without manual steps.
Goal: Fully automate the release process.

37) Typical pipeline stages?
Answer:
Checkout → install deps → lint → unit tests → build → security scan → package → deploy to staging → integration tests → manual approval → deploy to prod.
38) How do you do blue/green or canary releases?
Answer:
Run two environments. Switch traffic gradually. Roll back fast if errors increase.
39) Secrets management in pipelines?
Answer:
Use GitHub Actions secrets/AWS Secrets Manager. Never store secrets in code or logs.
40) Rollback strategy?
Answer:
Keep previous artifacts and DB backups. Use feature flags. Automated rollback on health check failure.
Sprint Planning & Agile - 
41) How do you plan a sprint?
Answer:
Define sprint goal, refine backlog, estimate (story points), consider capacity, pick stories, break into tasks, agree on Definition of Done.
42) How do you estimate work?
Answer:
Use story points (relative size). Refer to past velocity. Split large items into smaller ones.
43) How do you handle blockers?
Answer:
Raise early in standup, assign owner, find workaround, re-prioritize if needed.
44) How do you keep stakeholders aligned?
Answer:
Weekly demos, clear progress reports, early feedback, and transparent risks.
45) How do you measure success?
Answer:
Business metrics (conversion, retention), technical metrics (latency, error rate), team metrics (velocity, carryover).
________________________________________

System Design (Full-Stack)
46) Design a scalable file upload service.
Answer (short):
Frontend uploads to S3 via pre-signed URLs → Node issues URLs and records metadata in PostgreSQL → CloudFront serves files → Virus scan via Lambda → Use lifecycle policies and encryption → Monitor with CloudWatch.
47) Design an API for analytics dashboards.
Answer (short):
Ingest events (Kafka/Kinesis) → store raw in S3 → process with Lambda/ETL to Postgres (for live) and Redshift/Athena (for heavy queries) → cache frequently used aggregates (Redis) → secure with OAuth/JWT.

What technologies did you use in your DHP layer?
Answer:
We used Node.js (Express/NestJS) to build REST APIs, integrated with MongoDB/MySQL for temporary data storage, and Kafka/RabbitMQ for async communication between microservices. For security, we implemented JWT tokens and API Gateway policies. The DHP exposed unified APIs to the frontend (React) while managing multiple backend integrations behind the scenes.
How does the DHP handle data transformations?
Answer:
The DHP acted as a translator between different systems. For example, external services returned data in XML or custom JSON structures, and the DHP standardized it into a common API response format for the frontend. We used DTOs (Data Transfer Objects) and mapping utilities to achieve this consistently.

What was the coding challenge in your last project, and how did you resolve it?
how to do nodejs and reactjs integration? exaplain with example?

Step 1: Setup Node.js Backend
1.	Create a folder server
2.	Initialize project:
mkdir server && cd server
npm init -y
npm install express cors

Step 2: Setup React.js Frontend
1.	Create React app:
npx create-react-app client
cd client
npm start
Inside client/src/App.js:

export default App;
Start React app:
npm start
Proxy Setup (Optional, for cleaner API calls)
Instead of writing full URL (http://localhost:5000), set a proxy in client/package.json:
"proxy": http://localhost:5000
Now React can call API like:
fetch("/api/message")

How to integrate nodejs with db like mongodb or mysql? 
Option 1: Node.js + MongoDB (using Mongoose)
Step 1: Install packages
npm install express mongoose
Step 2: Setup server.js

Option 2: Node.js + MySQL (using mysql2)
Step 1: Install packages
npm install express mysql2
Step 2: Setup server.js

Frontend (React)
Inside React app (client/src/App.js):

export default App;

How to do gateways for Razorpay with nodejs and reactjs?
Step 1: Setup Razorpay Account
1.	Sign up at https://razorpay.com.
2.	Get your Key ID and Key Secret from the Dashboard → Settings → API Keys.
Step 2: Backend (Node.js + Express)
Install dependencies
npm install express razorpay body-parser cors

changes in server.js

Step 3: Frontend (React.js)
Install Razorpay Checkout Script
In public/index.html add:

