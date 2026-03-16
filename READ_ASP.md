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

