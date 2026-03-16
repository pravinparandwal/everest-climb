For a senior Node.js developer with 9 years of experience, interviews focus less on syntax and more on architecture, performance, security, and real-world problem-solving. The questions will probe your understanding of the "why" behind Node.js patterns and your experience with large, complex systems.

What is stream?
In Node.js, a Stream is a powerful concept used to handle reading and writing data efficiently — especially when dealing with large data like files, network responses, or video/audio streams.
Instead of reading or writing the entire data at once (which can be slow and memory-heavy), streams process data chunk by chunk — like a pipeline.
Why use Streams?
Because they:
•	Handle large data efficiently (no need to load the entire file into memory)
•	Improve performance and speed
•	Are asynchronous (non-blocking)
•	Support piping (chaining operations like Unix pipes)

Types of Streams in Node.js
1.	Readable Stream – used for reading data
Example: fs.createReadStream()
2.	Writable Stream – used for writing data
Example: fs.createWriteStream()
3.	Duplex Stream – both readable and writable
Example: net.Socket
4.	Transform Stream – duplex stream that can modify data
Example: zlib.createGzip() (for compression)


What is in chunk and by chunk data?
Chunk - When Node.js reads or writes a file (or any data stream), it does not take the whole file at once.
Instead, it divides the data into smaller parts, called chunks, and processes them one by one.
Example Explanation
Imagine you have a 1GB video file.
This will load the entire 1GB file into memory before doing anything.
If you have limited RAM, your app could crash or slow down.
Here, Node.js will:
•	Read a small piece (chunk) of the file (e.g., 64KB by default)
•	Emit a 'data' event for each chunk
•	Process it immediately
•	Then move to the next chunk — until the file is done
So, it doesn’t load the full file into memory — just a bit at a time.
Chunk - A small piece of the total data
By chunk - Means processing data piece by piece instead of all at once

How SSO work in nodejs?
How SSO Works — Conceptual Flow
Here’s a simplified step-by-step flow for SSO with Node.js backend:
1.	User tries to access App A.
o	App A redirects the user to the SSO authentication server (e.g., Auth0, Okta, or Custom Identity Provider).
2.	User logs in once on the SSO server (enters username/password).
3.	SSO Server validates credentials
o	If valid → generates a token (JWT, SAML, or OAuth2 access token).
o	The token includes user info and roles (claims).
4.	SSO server redirects user back to the Node.js app (App A) with that token.
5.	Node.js app verifies the token (via public key or secret).
o	If valid, creates a session or stores the token in cookies/local storage.
6.	When the user visits App B, it detects the valid SSO token → no need to log in again.

How have you scaled a Node.js application to handle high traffic and millions of requests? What architectural patterns and tools did you use? 
Answer:
•	Horizontal Scaling: Implement load balancing using tools like Nginx or a cloud-based solution to distribute traffic across multiple Node.js instances. Use stateless services where session data is stored in an external cache like Redis, allowing any instance to handle any request.
•	Clustering: Use the built-in cluster module to fork multiple worker processes, leveraging all available CPU cores on a single machine. Explain the role of the master process in managing workers and handling restarts in case of a crash.
•	Microservices: Describe your experience breaking down a large monolithic application into smaller, independently deployable microservices based on domain-driven design. Mention the advantages (scalability, fault isolation) and challenges (inter-service communication, data consistency).
•	Caching: Implement caching strategies to reduce database load. This could involve using a memory store like Redis to cache frequently accessed data or HTTP caching headers for client-side caching.

Explain the difference in execution order between process.nextTick(), setImmediate(), and setTimeout(fn, 0). 
Answer:
•	process.nextTick(): Executes its callback in the same phase of the event loop, immediately after the current operation finishes but before any I/O callbacks or timers run. It prioritizes the task for immediate execution.
•	setImmediate(): Schedules the callback to be executed in the next iteration of the event loop, specifically in the "check" phase. It is useful for running I/O-dependent code.
•	setTimeout(fn, 0): Schedules the callback to be executed after the minimum timer threshold has elapsed. It runs in the "timers" phase of the event loop. While often scheduled with a 0ms delay, it will still execute after any process.nextTick() callbacks and potentially after setImmediate() in the next event loop tick.

Question: How do you detect and fix a memory leak in a Node.js application in production? 
Answer:
•	Detection: Use a monitoring tool like PM2 or New Relic to track memory usage over time. If you notice a steady increase that doesn't stabilize, it's a red flag. For deeper analysis, use heapdump to take memory snapshots or the built-in perf_hooks for monitoring.
•	Debugging: Explain how to analyze memory snapshots with Chrome DevTools' Memory tab to find detached objects or objects that are not properly garbage-collected.
•	Solution: Identify common causes like unclosed database connections, long-lived timers or event listeners that are not properly cleaned up, or holding large objects in memory longer than necessary. The solution might involve using WeakMap or ensuring proper cleanup.

How do you handle rate limiting in Node.js APIs?
Answer:
I use middleware like express rate limit to control how many requests a user can make. For distributed systems, I use Redis to store request counts.

How do you manage environment variables securely?
Answer:
I use .env files locally and AWS Secrets Manager or SSM Parameter Store in production. I never commit secrets to Git.

What is ORM in node.js? 
ORM stands for Object Relational Mapping. 
In Node.js, an ORM is a library that lets you interact with a relational database (like PostgreSQL, MySQL, SQL Server, or SQLite) using JavaScript/TypeScript objects instead of writing raw SQL. It maps your models/classes to database tables and provides a high-level API for CRUD, relations, migrations, and often schema management.

What is ODM? (Object Document Mapper)
It is a library used to interact with NoSQL document databases, mainly MongoDB, using JavaScript/TypeScript objects.
ODM is used for NoSQL databases like MongoDB to manage documents, not tables.
Difference:
ORM is used to map JS objects to relational database tables (SQL), while ODM maps JS objects to NoSQL document databases like MongoDB.

What are some advanced 1security best practices you would implement in a production Node.js application? 
Answer:
•	Input Validation and Sanitization: Use a robust library like express-validator to validate and sanitize all user input, preventing injection attacks.
•	Dependency Management: Regularly scan for known vulnerabilities in third-party packages using npm audit.  Lock dependencies using package-lock.json and consider using npm ci in CI/CD pipelines.
•	Secure Headers: Use the helmet middleware to set a variety of HTTP headers that protect against common attacks like XSS.
•	Rate Limiting: Implement rate-limiting middleware (express-rate-limit) to protect against brute-force and Denial-of-Service (DoS) attacks.
•	Protect Secrets: Never hardcode secrets. Use environment variables (via .env in development) and secure secret management services (like AWS Secrets Manager) in production.

Question: You are building a new application from scratch. What criteria would you use to choose a database (SQL vs. NoSQL) and an ORM/ODM (Object-Relational Mapper / Object-Document Mapper)?
Answer:
•	Database Selection (SQL vs. NoSQL):
o	SQL (e.g., MySQL, PostgreSQL): Choose for applications with complex transactions, rigid data structures, or a strong need for data consistency (ACID compliance).
o	NoSQL (e.g., MongoDB, Redis): Choose for high scalability, flexible schemas, or when dealing with large volumes of unstructured data.
•	ORM/ODM Selection:
o	ORM (e.g., Sequelize): Use with SQL databases to abstract away raw queries, manage schema migrations, and simplify data interactions.
o	ODM (e.g., Mongoose): Use with MongoDB to provide schema validation and a more structured way to interact with the database.
•	Rationale: Emphasize that the choice depends on the project's specific needs, including data structure, consistency requirements, and scaling goals. For example, a financial application might require the strong consistency of SQL, while a social media app might prefer the flexibility and scalability of NoSQL

What is the difference between synchronous and asynchronous code in Node.js?
Answer:
Synchronous code runs one step at a time and blocks the thread. 
Asynchronous code uses callbacks, promises, or async/await to run tasks without blocking.


What is 1libuv in Node.js?
libuv is a C++ library used by Node.js to handle asynchronous operations like file system access, networking, timers, and the event loop.
It provides Node.js with a cross platform, non blocking I/O layer so JavaScript can remain single threaded but still perform async operations efficiently.
Why libuv Exists?
JavaScript is single threaded, but backend applications need:
•	File system operations
•	Network communication
•	DNS lookups
•	Timers
•	Async operations
•	Thread pools
libuv makes all this possible without blocking the main thread.
Why does Node.js need libuv?
Because JavaScript is single threaded, but server applications need to handle many concurrent operations. libuv provides async, non blocking behavior using an event loop and thread pool
Does Node.js become multi threaded because of libuv?
Yes, internally. Node.js itself runs JS on a single thread, but libuv uses a thread pool for background tasks.

Explain the Node.js 1event loop and how it handles concurrency?
Node.js uses a single-threaded event loop to handle asynchronous operations efficiently. 
The Event Loop is the mechanism that allows Node.js to perform non-blocking I/O operations. 
The event loop processes callbacks in phases (like timers, I/O, and setImmediate) and handles microtasks (process.nextTick, Promises) after each phase. 
Microtasks vs. Macrotasks 
Beyond phases, Node has two special microtask queues that run between task callbacks and after each callback completes, before the event loop advances phases:
•	Microtasks: 
o	process.nextTick queue (Node-specific): runs before other microtasks.
o	Promise microtask queue (.then/.catch/.finally).
•	Macrotasks: 
o	Timers (setTimeout/Interval)
o	setImmediate
o	I/O callbacks (from poll)
o	etc.

This architecture enables concurrency by allowing multiple operations to progress without blocking the main thread.
Note - Node.js is concurrent, not parallel — unless you use Worker Threads or child processes.

What are 1worker threads and when would you use them over child processes?
Worker Threads module enables the use of thread that execute in parallel. 
They’re ideal for CPU-intensive tasks like image processing, data processing, or mathematical computations. 
Worker Threads share memory and are more lightweight.
Use Worker Threads when you need high-performance parallelism within the same Node.js process, and Child Processes when you need process isolation or to run different scripts independently.
Worker Threads-
Use case: For CPU-intensive tasks like data processing, image manipulation, or mathematical computations — where you want to offload work without blocking the main thread.
Child Processes-
Use case: For running separate Node.js scripts, external commands, or when you need process isolation (e.g., restarting a crashed service independently).

How do you handle CPU-intensive tasks in Node.js?
To handle CPU-intensive tasks in Node.js — like image processing, data crunching, or complex calculations — you should offload the work from the main thread to avoid blocking the event loop. 
Use Worker Threads
Worker Threads run JavaScript in parallel on separate threads within the same process.

What is 1Clustering in Node.js?
Clustering in Node.js means using all the CPU cores of your computer to make your app faster. Instead of running just one process, Node.js can create multiple "worker" processes. These workers all run at the same time and share the same server port. Each worker is like a separate copy of your app, with its own memory and tasks, so they don’t interfere with each other.
How Clustering Improves Performance - 
Node.js is single-threaded by default, which means it can only use one CPU core. Clustering helps scale your application by:
•	Utilizing all CPU cores for parallel processing.
•	Handling more concurrent requests by distributing load across workers.
•	Improving fault tolerance - if one worker crashes, others continue running. 

Difference Between Cluster and Worker Threads?
 Cluster → multiple Node.js processes 
Worker Threads → multiple threads within the same process
“Cluster is used for scaling Node.js servers by creating multiple processes, while Worker Threads are used for running CPU-heavy tasks in parallel within a single process.”

5. What are common 1design patterns used in Node.js applications?
 Module Pattern
Encapsulates code into reusable modules using require or import.
Keeps code organized, promotes reusability and separation of concerns.
Singleton Pattern
Ensures a class has only one instance and provides a global point of access.
Useful for shared resources like configuration or database connections.
Factory Pattern
Creates objects without specifying the exact class/type.
Simplifies object creation logic, especially when dealing with multiple types.
Observer Pattern
Allows one object to notify others about changes (event-driven).
Perfect for handling asynchronous events in Node.js.
Middleware Pattern
Used heavily in frameworks like Express.js to process requests in layers.
Allows modular request handling and chaining of logic.
Proxy Pattern
Intercepts and controls access to another object.
Useful for logging, validation, or lazy loading.
 
6. How do you 1secure a Node.js API (e.g., authentication, authorization, CSRF, CORS, input validation)?
 Authentication & Authorization
•	Use JWT (JSON Web Tokens) or OAuth for secure user authentication.
•	Implement role-based access control (RBAC) to restrict access to sensitive endpoints.
Example – 
// Example: JWT middleware
const jwt = require('jsonwebtoken');
function authMiddleware(req, res, next) {
  const token = req.headers.authorization?.split(' ')[1];
  if (!token) return res.status(401).send('Unauthorized');
  try {
    const user = jwt.verify(token, process.env.JWT_SECRET);
    req.user = user;
    next();
  } catch (err) {
    res.status(403).send('Invalid token');
  }
}
Input Validation & Sanitization
•	Use libraries like Joi, express-validator, or zod to validate incoming data.
•	Prevent injection attacks (e.g., SQL, NoSQL, XSS).
HTTPS & Secure Headers
•	Always serve your API over HTTPS.
•	Use helmet to set secure HTTP headers.
CORS Configuration
•	Use cors to control which domains can access your API.
Secure Data Storage
•	Hash passwords using bcrypt.
•	Never store sensitive data (like tokens or passwords) in plain text.
Logging & Monitoring
•	Use tools like Winston, Morgan, or external services (e.g., Datadog, Sentry) to monitor API activity and errors.
Error Handling
•	Avoid exposing internal errors or stack traces to clients.
•	Use centralized error handling middleware.

What’s the difference between process.nextTick(), setImmediate(), and setTimeout()?
 process.nextTick()
•	Executes after the current operation, before the event loop continues.
•	Used for microtasks and prioritizing callbacks.
Use when you need to run code immediately after the current function finishes, before I/O or timers
setTimeout(fn, 0)
•	Executes in the timers phase of the event loop.
•	Schedules a callback after a minimum delay (not exactly 0ms).
Use for delaying execution or scheduling tasks.
setImmediate(fn)
•	Executes in the check phase of the event loop.
•	Runs after I/O events, but before setTimeout() if scheduled during I/O.
Use for deferring execution until the current poll phase is complete.
 
8. How would you implement rate limiting in a Node.js API?
 To implement rate limiting in a Node.js API, you can use middleware to restrict the number of requests a client can make within a specific time window. This helps prevent abuse, brute-force attacks, and server overload.
Using express-rate-limit (Most Common Approach)
1. Install the package
npm install express-rate-limit
Apply middleware in your Express app
// Define rate limit rule
const limiter = rateLimit({
  windowMs: 15 * 60 * 1000, // 15 minutes
  max: 100, // limit each IP to 100 requests per windowMs
  message: 'Too many requests, please try again later.',
});
How It Works
•	Each IP address is tracked.
•	If it exceeds the allowed number of requests within the time window, further requests are blocked temporarily.
•	You can customize limits per route, user role, or API key.
 



9. How do you handle error management in Node.js?
Use try/catch for synchronous code and .catch() or error middleware for async code.
Handle Errors in Async Code -
Use .catch() with Promises or try...catch in async/await.
Centralized Error Handling Middleware (Express)
app.use((err, req, res, next) => {
  console.error(err.stack);
  res.status(500).json({ error: 'Something went wrong!' });
});
Place this after all routes to catch unhandled errors.
Graceful Shutdown
Ensure resources (e.g., DB connections) are closed properly on fatal errors.

What are the different error 1codes?
While GraphQL often returns 200 OK even with errors, many teams want transport to reflect semantics:

REST APIs, error codes fall under 4xx (client errors) and 5xx (server errors).
Client Error Codes (4xx)
400 – Bad Request
Malformed request syntax, invalid JSON, missing required fields.
401 – Unauthorized
Authentication required or failed.
403 – Forbidden
Client authenticated but not allowed.
404 – Not Found
Requested resource does not exist.
409 – Conflict
Data conflict — e.g., duplicate records.
Other:
402 – Payment Required
Rarely used; reserved for future use.
405 – Method Not Allowed
HTTP method not supported for the route.
406 – Not Acceptable
Resource cannot produce acceptable content per Accept headers.
407 – Proxy Authentication Required
Client must authenticate with proxy.
408 – Request Timeout
Server timed out waiting for the request.
409 – Conflict
Data conflict — e.g., duplicate records.
410 – Gone
Resource is permanently removed.
411 – Length Required
Content-Length header missing.
412 – Precondition Failed
Preconditions in request headers failed.
413 – Payload Too Large
Request body too big.
414 – URI Too Long
URL exceeds maximum length.
415 – Unsupported Media Type
Server cannot handle request payload format.
416 – Range Not Satisfiable
Requested content range not valid.
417 – Expectation Failed
Expect header cannot be met.
418 – I’m a teapot (fun code)
Defined in RFC 2324 (used jokingly).
421 – Misdirected Request
Request sent to server not capable of handling it.
422 – Unprocessable Entity
Validation errors (common in APIs).
423 – Locked
Resource is locked.
424 – Failed Dependency
Dependent request failed.
425 – Too Early
Server unwilling to process risked replay.
426 – Upgrade Required
Client must upgrade protocol.
428 – Precondition Required
Server requires request conditions (for concurrency).
429 – Too Many Requests
Rate limiting.
431 – Request Header Fields Too Large
Headers too large.
451 – Unavailable For Legal Reasons
Blocked due to legal restrictions.

Server Error Codes (5xx)
500 – Internal Server Error
Generic server crash or unexpected error.
502 – Bad Gateway
Upstream server returned an invalid response.
503 – Service Unavailable
Server temporarily overloaded/maintenance.
504 – Gateway Timeout
Upstream server timed out.

Others:
501 – Not Implemented
Server doesn’t support the functionality.
505 – HTTP Version Not Supported
Unsupported HTTP version.
506 – Variant Also Negotiates
Configuration error in transparent content negotiation.
507 – Insufficient Storage
Server cannot store representation.
508 – Loop Detected
Infinite loop detected in server.
510 – Not Extended
Further extensions required.
511 – Network Authentication Required
Client must authenticate to access network.


Example1:
app.get("/user/:id", (req, res) => {
  const user = null;
  if (!user) {
    return res.status(404).json({ error: "User not found" });
  }
  res.json(user);
});
Example2:
app.use((err, req, res, next) => {
  console.error(err);
  const status = err.status || 500;
  res.status(status).json({
    success: false,
    message: err.message || "Internal Server Error",
  });
});

What is primitives in node.js?
In Node.js (which is built on JavaScript), primitive types are the most basic, immutable data types. They are not objects, don’t have methods, and are stored by value instead of by reference.
Primitive Types:
1.	String:
2.	Number
3.	Boolean
4.	Null
5.	Undefined: A variable declared but not assigned any value.
6.	BigInt: Used for integers larger than the Number limit.
7.	Symbol: Used to create unique identifiers
“In Node.js, primitives are basic, immutable data types such as string, number, boolean, null, undefined, bigint, and symbol. They are stored by value, not by reference, which means modifying one variable doesn’t affect another. Primitives are fast, lightweight, and form the foundation for all other complex data structures.”

What is 1Middleware in Express?
Middleware is a function that has access to the request (req), response (res), and the next middleware function (next) in the request-response cycle.
Middleware is like a pipeline of functions that process an incoming HTTP request before it reaches your actual route handler.
 It can:
•	Execute any code
•	Modify req or res
•	End the request-response cycle
•	Call next() to pass control to the next middleware
Common Use Cases
•	Logging
•	Authentication
•	Error handling
•	Request parsing
•	Rate limiting
•	CORS setup
Types of Middleware
1.	Application-level middleware
o	Defined using app.use() or app.METHOD() (e.g., app.get)
o	Example: logging, authentication, validation
2.	Router-level middleware
o	Works with express.Router()
o	Used for modular route management
3.	Built-in middleware
o	Express provides some built-in middleware like:
	express.json() → parses incoming JSON request
	express.urlencoded() → parses form data
4.	Error-handling middleware
o	Has 4 parameters: (err, req, res, next)
o	Example: global error handler
5.	Third-party middleware
o	External libraries like morgan, cors, helmet

Common Middleware We Use in Node.js
Here are the most popular ones (you can mention these in interviews):
•	express.json() → to parse JSON requests
•	express.urlencoded() → to parse form data
•	cors → to enable Cross-Origin Resource Sharing
•	helmet → to secure HTTP headers
•	morgan → for logging requests
•	cookie-parser → for handling cookies
•	express-session → for session handling
•	body-parser (old, but still used) → to parse request bodies
•	compression → for response compression (gzip)
•	multer → for handling file uploads
Example
const express = require('express');
const app = express();
const morgan = require('morgan');
const cors = require('cors');

// Built-in middleware
app.use(express.json());

// Third-party middleware
app.use(morgan('dev'));
app.use(cors());

// Custom middleware
app.use((req, res, next) => {
  console.log(`Request URL: ${req.url}, Method: ${req.method}`);
  next(); // pass control to next middleware
});

// Route
app.get('/', (req, res) => {
  res.send('Hello Middleware!');
});

// Error-handling middleware
app.use((err, req, res, next) => {
  console.error(err.stack);
  res.status(500).send('Something broke!');
});
app.listen(3000, () => console.log('Server running on port 3000'));

11. Difference between CommonJS (require) and ES Modules (import) in Node.js?
 CommonJS (require) - 
Example – 
const fs = require('fs');
module.exports = myFunction;
Loading: Synchronously loaded modules.
Scope: Each file is its own module.
Default in Node.js: Historically the standard module system.
File Extension: .js (no special config needed).
Use Case: Works well in older Node.js versions and most existing projects.
ES Modules (import) - 
Example – 
import fs from 'fs';
export default myFunction;
Loading: Asynchronously loaded modules.
Scope: Strict mode by default.
Modern Standard: Based on the ECMAScript specification.
File Extension: .mjs or set "type": "module" in package.json.
Use Case: Preferred for modern JavaScript and compatibility with frontend code.
 
12. How do you manage configuration across multiple environments (dev, QA, prod)?
 Use Environment Variables
Store environment-specific settings (e.g., DB credentials, API keys) in .env files and load them using the dotenv package.
Example .env files:
•	.env.development
•	.env.qa
•	.env.production

equire('dotenv').config({ path: `.env.${process.env.NODE_ENV}` });
console.log(process.env.DB_HOST); // environment-specific value
Use a Config File Structure
Organize config settings in separate files per environment.
Example:
config/
  development.js
  qa.js
  production.js
  index.js
index.js -
const env = process.env.NODE_ENV || 'development';
const config = require(`./${env}`);
module.exports = config;
Use cross-env for Environment Setup in Scripts
Set NODE_ENV in your package.json scripts:
"scripts": {
  "start:dev": "cross-env NODE_ENV=development node app.js",
  "start:qa": "cross-env NODE_ENV=qa node app.js",
  "start:prod": "cross-env NODE_ENV=production node app.js"
}
Avoid Hardcoding Sensitive Data

13. How do you scale a Node.js application in AWS/Azure/GCP?
 Horizontal Scaling (Multiple Instances)
Run multiple instances of your Node.js app to handle more traffic.
•	AWS: Use Elastic Beanstalk, EC2 Auto Scaling, or ECS (Fargate).
•	Azure: Use App Service with scaling rules or AKS (Kubernetes).
•	GCP: Use App Engine, Compute Engine, or GKE (Kubernetes).
Load Balancing
Distribute incoming traffic across multiple instances.
•	AWS: Use Elastic Load Balancer (ELB).
•	Azure: Use Azure Load Balancer or Application Gateway.
•	GCP: Use Cloud Load Balancing.
Use Clustering in Node.js
Leverage multiple CPU cores using the built-in cluster module.
Stateless Architecture
Ensure your app is stateless so any instance can handle any request.
•	Store sessions in Redis, DynamoDB, or Cosmos DB.
•	Use object storage (e.g., S3, Blob Storage) for files.
Containerization
Package your app using Docker for portability and scalability.
•	Deploy to Kubernetes (EKS, AKS, GKE) or serverless containers.
Auto Scaling
Automatically adjust the number of instances based on traffic.
•	Set up CPU/memory-based scaling rules.
•	Use serverless platforms like AWS Lambda, Azure Functions, or GCP Cloud Functions for event-driven scaling.
Monitoring & Logging
Use cloud-native tools to monitor performance and errors.
•	AWS: CloudWatch, X-Ray
•	Azure: Application Insights
•	GCP: Stackdriver
Security & Configuration
•	Use environment variables for config.
•	Secure secrets using AWS Secrets Manager, Azure Key Vault, or GCP Secret Manager.

13. How to optimize 1performance in nodejs?
Ans - 1. Use Clustering
•	Run multiple instances of your app using all CPU cores.
•	Helps handle more requests in parallel.
2. Use Asynchronous Code
•	Avoid blocking operations like fs.readFileSync() or long loops.
•	Use async/await or callbacks to keep the event loop free.
3. Use a Reverse Proxy (like Nginx)
•	Offload tasks like SSL termination, caching, and load balancing.
•	Improves scalability and security.
4. Enable Caching
•	Cache frequent data (e.g., API responses, DB queries) using Redis or in-memory storage.
•	Reduces load and speeds up response time.
5. Optimize Database Queries
•	Use indexes, avoid unnecessary joins, and limit data fetched.
•	Use connection pooling for better performance.
6. Use Streams for Large Data
•	For file uploads/downloads or large data processing, use streams instead of loading everything into memory.
7. Monitor and Profile Your App
•	Use tools like PM2, New Relic, or Node.js built-in profiler to find bottlenecks.
•	Helps identify memory leaks or slow functions.
8. Minimize Middleware
•	Only use necessary middleware in Express or other frameworks.
•	Unused or heavy middleware can slow down request handling.
9. Use Environment-Specific Configs
•	Disable debugging and logging in production.
•	Use production-ready settings for performance.
10. Keep Dependencies Lean
•	Avoid bloated packages or unused modules.
•	Smaller codebase = faster startup and less memory usage.


14. How do you debug memory leaks or performance bottlenecks in Node.js?
 Use Built-in Profiling Tools
--inspect and Chrome DevTools
Start your app with:
node --inspect app.js
Then open chrome://inspect in Chrome to:
•	Take heap snapshots
•	Monitor memory usage
•	Analyze CPU profiles
Use clinic.js for Deep Analysis
Install - npm install -g clinic
Run - clinic doctor -- node app.js
It provides visual reports for:
•	CPU bottlenecks
•	Event loop delays
•	Memory leaks

Monitor Garbage Collection
Use the --trace-gc flag:
node --trace-gc app.js
This helps you understand how often and how effectively garbage collection is happening
 Use Heap Snapshots
Use v8 or Chrome DevTools to:
•	Take snapshots at different times
•	Compare retained objects
•	Identify memory leaks (e.g., event listeners not removed)

Use process.memoryUsage()
Track memory usage programmatically:
console.log(process.memoryUsage());
Common Causes of Memory Leaks
•	Unremoved event listeners
•	Global variables holding references
•	Closures retaining memory
•	Caching too much data
Fixing Performance Bottlenecks
•	Use clustering or worker threads for CPU-bound tasks
•	Optimize database queries
•	Use async operations properly
•	Profile hot paths with console.time() or DevTools

15. What are your strategies for logging and monitoring (e.g., Winston, Morgan, ELK stack)?
Logging Strategies
Logging helps you track application behavior, errors, and performance.
1. Use a Logging Library
•	Popular choices: winston, bunyan, pino
•	Supports log levels (info, warn, error), formatting, and transports (file, console, cloud)
2. Structured Logging
•	Log in JSON format for easier parsing and analysis.
•	Include metadata like timestamps, request IDs, user IDs.
3. Log Rotation
•	Use tools like logrotate or winston-daily-rotate-file to manage log size and retention.
Monitoring Strategies
Monitoring helps you detect issues, track performance, and ensure uptime.
1. Use APM Tools (Application Performance Monitoring)
•	Tools: New Relic, Datadog, Dynatrace, AppDynamics
•	Track response times, throughput, error rates, memory usage
2. Use Cloud-native Monitoring
•	AWS: CloudWatch
•	Azure: Application Insights
•	GCP: Stackdriver

What are Connectors in Node.js?
A connector is a module, library, or component that allows your Node.js application to connect and interact with another system such as:
•	Databases (MongoDB, MySQL, PostgreSQL, Oracle)
•	Cloud services (AWS S3, Azure Blob, GCP Pub/Sub)
•	Third-party APIs (Stripe, PayPal, Salesforce)
•	Messaging systems (Kafka, RabbitMQ)
Think of a connector as a bridge or adapter between Node.js and an external service.
InShort - Connectors in Node.js are modules that enable integration with external systems like databases, APIs, cloud services, and messaging platforms. For example, I’ve used mongoose as a MongoDB connector, mysql2 for MySQL, aws-sdk for AWS S3, and stripe for payments. They act as bridges, making communication between Node.js and external services seamless.
What is a Wrapper API?
A Wrapper API is an intermediary API that sits between the client (like React, Angular, Mobile App) and one or more backend/external services
Why Use a Wrapper API?
•	Simplifies frontend code → frontend doesn’t deal with multiple APIs directly.
•	Standardizes responses → no matter which backend service is used, output format is consistent.
•	Security → hides internal service details, applies authentication/authorization at one place.
•	Flexibility → if backend changes (e.g., from SOAP to REST), only wrapper updates, not frontend.
•	Rate limiting / caching → can improve performance.
Example
Scenario:
•	Your React frontend needs:
o	Customer details (from CRM API)
o	Transaction details (from Banking API)
o	Rewards points (from Loyalty API)
Without Wrapper API:
React app calls 3 different services, each with its own auth and data format.
With Wrapper API (Node.js Express example):
const express = require('express');
const axios = require('axios');
const app = express();

// Wrapper API endpoint
app.get('/api/user/:id', async (req, res) => {
  try {
    const userId = req.params.id;

    // Call multiple backend services
    const [customer, transactions, rewards] = await Promise.all([
      axios.get(`https://crm-service.com/users/${userId}`),
      axios.get(`https://banking-service.com/transactions/${userId}`),
      axios.get(`https://loyalty-service.com/rewards/${userId}`)
    ]);

    // Combine & standardize response
    res.json({
      user: customer.data,
      transactions: transactions.data,
      rewards: rewards.data
    });

  } catch (err) {
    res.status(500).json({ error: 'Internal Server Error' });
  }
});

app.listen(3000, () => console.log("Wrapper API running on 3000"));

InShort- A Wrapper API is an abstraction layer that consolidates multiple backend services and exposes a single, simplified API to clients. It helps with standardizing responses, improving security, and reducing frontend complexity. For example, in one of my projects, we built a Node.js wrapper API that combined data from CRM, payment, and loyalty services so the React frontend only needed to call one endpoint

Node.js — Scenario Q&A
5) Scenario: File uploads timeout and memory usage spikes.
Question: How would you redesign?
Answer:
•	Use streaming instead of buffering: req.pipe(...) to S3 via pre-signed URLs so browser uploads directly.
•	Validate file type/size before signing.
•	Move virus scan to Lambda async.
•	Return 202 Accepted + status endpoint if processing is async.
6) Scenario: Random crashes due to “out of memory”.
Question: What steps will you take?
Answer:
•	Enable heap snapshots and clinic.js profiling.
•	Look for unbounded arrays/maps, missing stream .pipe backpressure, or retry loops.
•	Enforce max listeners, close DB connections, and ensure await cleanup.
•	Add PM2 with restart policy + memory limits.
•	Write regression tests once root cause fixed.

How you use AI in project?
To speed up Node.js development and maintain standards, I use AI tools like GitHub Copilot and Cloude, Gemini, Amazon code whisper, ChatGPT for faster coding and generating boilerplate. 
For code quality, I rely on SonarQube with AI-based analysis and CodiumAI for automated test generation. These tools help improve productivity, ensure best practices, and reduce bugs while keeping coding standards consistent across the team.

What is GraphQL?
GraphQL is a query language for APIs and a runtime for executing those queries by using your existing data. Unlike REST, where you have multiple endpoints, GraphQL exposes a single endpoint that accepts queries specifying exactly what data is needed.
Why use GraphQL with Node.js and React?
•	Node.js: Acts as the backend server handling GraphQL requests.
•	React: Frontend client queries the backend through GraphQL.
•	GraphQL helps to avoid over-fetching or under-fetching data.
•	Easy to evolve APIs without breaking existing clients.
Step 1: Setup GraphQL Server in Node.js
We'll use:
•	express for server
•	express-graphql to integrate GraphQL middleware
•	graphql for schema and resolver

Step 2: Connect React to GraphQL Server
You can use libraries like Apollo Client to interact with GraphQL in React.
Basic React Setup with Apollo Client
1.	Install packages:
npm install @apollo/client graphql
Setup Apollo Client and perform queries/mutations

Questions:
How to manage multiple role in single table?
How to optimize performance in nodejs?
How work payment gateway?
How to handle real time communication in nodejs?
What are worker thread in nodejs?
Which architecture you prefer in nodejs? Like monolithic or microservice 
How we can write basic server in nodejs?
What is bidy parser in nodejs?
Write connections for db?
How authentication and authorization works?
What is web socket?
What is callback?
Diff between promis.all and promis.allSetter method?
Why is process.nextTick() is faster than setImediate()?
How does nodejs handle multiple CPU cores?
How do you prevent callback hell in nodejs?

1) Node.js Architecture & Event Loop
Q1. What is Node.js and why use it?
•	Answer (Interview point): 
o	Runtime built on V8 (Chrome’s JS engine).
o	Single-threaded, non-blocking I/O, optimized for I/O-bound and real-time apps.
o	Great for APIs, microservices, websockets, streaming.
Q2. How does the Event Loop work?
•	Answer: 
o	Manages phases: timers → pending callbacks → idle/prepare → poll → check → close callbacks.
o	I/O callbacks are queued; CPU isn’t blocked by I/O.
o	Microtasks (Promises, queueMicrotask) run after each phase and before next tick of loop.
Q3. process.nextTick() vs microtasks vs setImmediate()?
•	Answer: 
o	process.nextTick(): runs before microtasks (priority), can starve the loop if overused.
o	Microtasks (Promise.then): run after current stack, before moving to next event loop phase.
o	setImmediate(): runs in check phase; setTimeout(..., 0) runs in timers phase.
________________________________________
2) Modules & Package Management
Q4. CommonJS vs ES Modules in Node?
•	Answer: 
o	CommonJS: require, module.exports, default historically.
o	ESM: import, export, enabled via "type": "module" or .mjs.
o	No mixing imports/exports in the same file without interop flags.
Q5. What is package.json and key fields?
•	Answer: 
o	Metadata + dependencies + scripts.
o	Important fields: main, type, scripts, dependencies, devDependencies, engines.
o	Use npm ci in CI for reproducible installs (locks to package-lock.json).
________________________________________
3) Asynchronous Programming
Q6. Callbacks vs Promises vs async/await?
•	Answer: 
o	Callbacks: prone to callback hell and error handling complexity.
o	Promises: composable, .then/.catch.
o	async/await: cleaner control flow; always wrap with try/catch.
Q7. How to handle parallel async tasks safely?
•	Answer: 
o	await Promise.all([...]) for fail-fast parallelism.
o	Promise.allSettled for collect all results.
o	Control concurrency with pools (e.g., p-limit) or custom queue.
________________________________________
4) Streams & Buffers
Q8. What are Streams and why use them?
•	Answer: 
o	Process data chunk-by-chunk (memory efficient) for big files, network responses.
o	Types: Readable, Writable, Duplex, Transform.

Q9. Show a simple file read stream pipeline.
const fs = require('fs');
const zlib = require('zlib');

fs.createReadStream('input.txt')
  .pipe(zlib.createGzip())
  .pipe(fs.createWriteStream('input.txt.gz'))
  .on('finish', () => console.log('Done'));

Q10. What is Buffer?
•	Answer: 
o	A raw binary data container; used for I/O.
o	E.g., Buffer.from('hello'), beware of encoding issues.
________________________________________
5) HTTP, Express, and Middleware
Q11. How do you create a basic HTTP server without Express?
const http = require('http');
const server = http.createServer((req, res) => {
  res.writeHead(200, {'Content-Type':'application/json'});
  res.end(JSON.stringify({ ok: true }));
});
server.listen(3000);
``
Q12. What is middleware in Express?
•	Answer: 
o	Functions with signature (req, res, next) that run in order.
o	Used for logging, auth, parsing, validation, errors.

Q13. How to write an error-handling middleware?
app.use((err, req, res, next) => {
  console.error(err);
  res.status(err.status || 500).json({ error: 'Something went wrong' });
});

6) Error Handling & Reliability
Q14. Best practices for error handling in async code?
•	Answer: 
o	Always try/catch around await.
o	Return meaningful HTTP status codes.
o	Centralized error handler; never let unhandled promise rejections slip.
o	Use process.on('unhandledRejection') and process.on('uncaughtException') to log and exit gracefully.
Q15. Graceful shutdown in Node?
•	Answer: 
o	On SIGTERM/SIGINT, stop accepting new requests, finish in-flight, close DB, then process.exit(0).
________________________________________
7) Process, Clustering & Worker Threads
Q16. How to utilize multiple CPU cores?
•	Answer: 
o	Cluster module: forks multiple Node processes sharing the same port.
o	Worker Threads: run CPU-intensive JS in separate threads within one process.
o	Use PM2 or container orchestrators for production process management.
Q17. When to use Worker Threads over Cluster?
•	Answer: 
o	Use Workers for CPU-bound tasks (e.g., hashing, image processing).
o	Use Cluster for scaling I/O-bound servers.
________________________________________
8) File System, Path, Env
Q18. How to read a file with Promises API?
const fs = require('fs/promises');
const data = await fs.readFile('config.json', 'utf8');
Q19. Why use path.join instead of string concatenation?
•	Answer: 
o	Handles cross-OS path separators; prevents bugs.
Q20. Managing config and secrets?
•	Answer: 
o	Use environment variables (process.env), 12-factor app principles.
o	Never commit secrets; use secret managers or .env in dev.
9) Security Essentials
Q21. Common security best practices in Node APIs?
•	Answer: 
o	Use helmet, rate limiting, CORS rules.
o	Validate inputs (e.g., Joi/Zod), sanitize to prevent XSS/NoSQL injection.
o	Use parameterized queries for DB.
o	Keep dependencies updated; run npm audit, lockfile, and pin versions when needed.
Q22. How to handle JWT securely?
•	Answer: 
o	Short expiry, refresh tokens, store in httpOnly cookies if web, verify audience/issuer, rotate secrets.
________________________________________
10) Performance & Observability
Q23. How do you profile a Node app?
•	Answer: 
o	Use —inspect with Chrome DevTools, clinic.js, 0x, or APM tools.
o	Monitor event loop lag, memory, CPU, GC pauses.
Q24. Caching strategies?
•	Answer: 
o	In-memory (LRU for small hot data), distributed cache (Redis) for scale.
o	Cache headers for HTTP responses, ETag/Last-Modified.
Q25. Logging best practices?
•	Answer: 
o	Structured JSON logs (pino/winston), include correlation IDs, avoid PII, centralize logs (ELK/Datadog).
________________________________________
11) Testing
Q26. How to test async handlers?
•	Answer: 
o	Use Jest/Mocha with async tests.
o	Mock external I/O; test happy path + failure path; use supertest for HTTP.

it('returns 200', async () => {
  const res = await request(app).get('/health');
  expect(res.status).toBe(200);
});

12) Database Connections
Q27. How to manage DB connections in Node?
•	Answer: 
o	Use connection pools; reuse clients.
o	Close pool on shutdown.
o	Backoff + retry for transient errors.
o	Use migrations (e.g., knex, sequelize, prisma).
________________________________________
13) Child Processes & Events
Q28. Difference between child_process and worker_threads?
•	Answer: 
o	child_process: separate process; IPC via stdio/message; good for legacy/CLI tasks.
o	worker_threads: same process, separate thread; share memory with SharedArrayBuffer.
Q29. How does EventEmitter work?
•	Answer: 
o	Publish/subscribe pattern; on, emit, once.
o	Remember to remove listeners to avoid memory leaks.
________________________________________
14) Common Pitfalls
Q30. What causes “Event loop blocked” and how to avoid it?
•	Answer: 
o	Heavy synchronous CPU tasks on main thread.
o	Offload to worker_threads, optimize or chunk work with setImmediate.
Q31. Why is await in a loop sometimes bad?
•	Answer: 
o	Serializes tasks; use Promise.all for true parallel I/O.

