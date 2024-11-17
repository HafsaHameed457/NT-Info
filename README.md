# Nodejs-interview-questions

## What is node js
The Node.js runtime is an environment that allows JavaScript to run on the server, outside of a web browser. Built on the V8 JavaScript engine (from Google Chrome), Node.js is fast and efficient at executing JavaScript code.


## Key Components of Node.js Runtime:

1. JavaScript Engine (V8): Compiles and runs JavaScript code, optimizing for high performance.

2. Event Loop: Manages asynchronous operations, handling multiple tasks (like file operations, network requests) without blocking the main thread.

3. Non-Blocking I/O: Uses asynchronous, non-blocking input/output operations to handle multiple requests simultaneously, making it ideal for real-time applications.

4. Built-in Modules: Provides core modules (like fs for file systems, http for creating servers) that offer common functionalities directly, without needing third-party libraries.

## Why Node.js?

Node.js’s runtime allows developers to use JavaScript on both the front end and back end, creating full-stack applications with a single language. Its non-blocking, event-driven architecture is particularly suited for building scalable applications, like APIs, real-time chat apps, and microservices.

## Difference between backend and frontend

The frontend is the part of a web application that users interact with directly — it includes everything users see, click, or type (HTML, CSS, JavaScript).

The backend is the server-side part that handles data processing, storage, and business logic — it manages databases, server operations, and APIs that communicate with the frontend.

## Difference between NODE JS AND JAVASCRIPT

JavaScript:

1. Runs in the browser (e.g., Chrome, Firefox).

2. Primarily used for frontend development, manipulating the DOM and handling user interactions.

3. Limited to browser capabilities (no direct access to files, OS, or network outside the browser).

Node.js:

1. A runtime environment that allows JavaScript to run on the server.

2. Used for backend development, building APIs, servers, and handling file systems.

3. Has access to the operating system, file system, and network, thanks to built-in modules like fs, http, etc.


## What is Deno?

Deno is a secure runtime for JavaScript and TypeScript, created by the same developer who built Node.js. It is designed to address some of Node.js’s shortcomings. Here are key features of Deno:

1. Security: Deno runs with a secure sandbox by default, where access to the file system, network, or environment variables requires explicit permission.

2. TypeScript Support: Deno has built-in TypeScript support without the need for external tools or transpilers.

3. Single Executable: Deno is distributed as a single executable with no package manager like npm. Instead, it directly imports modules via URLs.

4. Modern Features: It uses modern JavaScript and TypeScript features, with support for async/await, ES modules, and promises.

5. Deno aims to provide a more secure, modern, and efficient environment for server-side JavaScript and TypeScript development.

## Node vs Deno

| Feature                      | **Node.js**                                    | **Deno**                                      |
|------------------------------|------------------------------------------------|-----------------------------------------------|
| **Runtime**                  | Runs JavaScript on the server (V8 engine)      | Runs JavaScript and TypeScript on the server (V8 engine) |
| **Security**                 | No built-in security model, full access to OS | Secure by default, requires explicit permissions for file, network, and environment access |
| **Package Management**       | Uses npm for managing packages and modules     | No package manager; imports modules directly via URLs |
| **Modules**                  | Uses CommonJS (with experimental ES Modules)   | Fully supports ES Modules (import/export syntax) |
| **TypeScript Support**       | Requires external tools like Babel or TypeScript compiler | Native support for TypeScript without configuration |
| **API**                      | Rich set of APIs for file system, networking, etc. | Limited API (focused on security and modern JS features) |
| **Single Executable**        | Requires Node.js installation and npm for modules | Distributed as a single executable with no external dependencies |
| **Community and Ecosystem**  | Large ecosystem with millions of packages      | Smaller, newer ecosystem but growing quickly |
| **Popularity**               | Well-established and widely used               | Newer, with growing interest in modern applications |


## Global Object

In JavaScript, the global object is an object that provides access to various global variables and functions. It acts as the top-level container for all variables and functions that are available in the global scope.

### Global Object in Different Environments:
- In a browser:

The global object is window.
It provides access to browser-specific features like document, localStorage, and console.
javascript
Copy code
console.log(window); // The global object in browsers

- In Node.js:

The global object is global.
It provides access to Node.js-specific features like __dirname, module, and process

- Some global properties/functions in JavaScript, such as setTimeout, console, and Math, are part of the global object.

## Synchronous and Asynchronous

| Feature                        | **Synchronous**                              | **Asynchronous**                              |
|--------------------------------|---------------------------------------------|----------------------------------------------|
| **Execution**                  | Tasks are executed one after another, in order. | Tasks are executed independently of the main thread. |
| **Blocking**                   | Blocks further execution until the current task completes. | Does not block execution; other tasks can run while waiting. |
| **Performance Impact**         | Can cause delays if a task takes time, as it blocks other tasks. | More efficient for time-consuming tasks (e.g., I/O operations). |
| **Example**                    | `console.log('A'); console.log('B');`      | `setTimeout(() => console.log('A'), 1000); console.log('B');` |
| **Use Case**                   | Suitable for small, fast tasks that don't involve waiting (e.g., simple calculations). | Ideal for tasks that take time or require waiting (e.g., API requests, file I/O). |
| **Flow Control**               | Executes sequentially, one after another.  | Tasks are initiated and their results handled later, usually with callbacks or promises. |

## Asynchrnous callbacks or callbacks

Asynchronous callbacks are functions that are passed as arguments to other functions and are executed after a certain task or event has completed. They allow JavaScript to handle tasks that take time (like reading files, making API requests, or handling user input) without blocking the execution of other code.

## Multi-threading, Processes, and Threads in Computing

- Multi-threading:
Multi-threading refers to the ability of a CPU (Central Processing Unit) or a single core within a CPU to execute multiple threads concurrently. A thread is the smallest unit of a process that can be scheduled to run. Multi-threading enables tasks to be divided into smaller units (threads) that can run in parallel, improving efficiency, especially in multi-core processors.

Example: Running multiple tasks like downloading a file, processing data, and updating the UI simultaneously in a program.

- Process:
A process is an instance of a program that is being executed. It has its own memory space, system resources, and at least one thread of execution. Processes are independent of each other and do not share memory space (unless using inter-process communication). Processes are typically more resource-intensive than threads.

Example: When you open a browser, an instance of the browser program running is a process.

- Thread:
A thread is a smaller unit of a process that can run independently. Multiple threads within a process share the same memory space and resources, allowing them to communicate more easily and efficiently. Threads are lighter-weight compared to processes and are typically used to perform tasks concurrently within a process.

Example: A web server process can have multiple threads to handle different client requests at the same time.

## Node js vs Python vs PHP

| Feature                        | **Node.js**                              | **PHP**                                       | **Python**                                   |
|---------------------------------|------------------------------------------|-----------------------------------------------|----------------------------------------------|
| **Runtime**                     | V8 JavaScript engine                     | PHP interpreter                               | Python interpreter                           |
| **Primary Use Case**            | Server-side JavaScript execution         | Web development, server-side scripting        | General-purpose, web development, data science |
| **Language**                    | JavaScript                               | PHP (Hypertext Preprocessor)                  | Python                                       |
| **Concurrency Model**           | Non-blocking, Event-driven (single-threaded with async I/O) | Multi-threaded, synchronous                   | Multi-threaded, synchronous with async capabilities (asyncio) |
| **Performance**                 | High performance, especially for I/O-intensive applications | Moderate, often slower for large-scale applications | High for computation-heavy tasks, moderate for I/O-intensive tasks |
| **Package Management**          | npm (Node Package Manager)               | Composer (for PHP dependencies)               | pip (Python Package Index)                   |
| **Community & Ecosystem**       | Large ecosystem with many JavaScript modules | Mature ecosystem, especially in web development | Large, with robust libraries for machine learning, data science, and web development |
| **Learning Curve**              | Moderate (JavaScript knowledge required) | Easy (based on C-like syntax)                 | Easy to learn, highly readable syntax        |
| **Support for Web Frameworks**  | Express.js, Koa.js, NestJS               | Laravel, Symfony, CodeIgniter                 | Django, Flask, FastAPI                       |
| **Use in Full-Stack Development**| Popular in full-stack with JavaScript (MEAN, MERN stacks) | Common in LAMP stack (Linux, Apache, MySQL, PHP) | Used with Django or Flask for full-stack development |
| **Best for**                    | Real-time applications, APIs, and I/O-intensive systems | Traditional web applications, content management systems | Web apps, data science, scripting, and automation |

## Observer Pattern

The Observer design pattern is a behavioral design pattern that defines a one-to-many dependency between objects. In this pattern, when the state of one object (called the subject) changes, all its dependent objects (called observers) are notified automatically. This is particularly useful in scenarios where multiple components need to stay in sync with a single data source or state.

Real-World Example:
A real-world example of the Observer pattern is a news agency and its subscribers:

- The news agency (subject) has several subscribers (observers).
- Whenever the news agency updates or publishes new content, all its subscribers are notified with the latest news.


## Structure of Observer Pattern:
Subject (or Observable): The object that maintains a list of observers and notifies them about changes to its state.
Observer: The objects that need to be notified when the subject's state changes.
ConcreteSubject: A specific implementation of the subject that notifies observers of state changes.
ConcreteObserver: A specific implementation of the observer that reacts to the updates from the subject.

## Event emitter in NODE js

The EventEmitter class in Node.js is a core module that enables the event-driven programming model. It allows objects (often called "emitters") to emit events and have listeners (or "handlers") to respond to those events. It is used to handle asynchronous events and helps in creating flexible and modular systems where different parts of the application can react to specific events.

#### code for events 

const EventEmitter = require('events');

const myEmitter = new EventEmitter();
myEmitter.on('greet', () => {
  console.log('Hello, world!');
});

myEmitter.emit('greet');  // Output: Hello, world!


## Why we use modules?

Modules in Node.js help organize code, reuse functionality, and avoid namespace conflicts. They allow you to split code into manageable parts, use built-in and third-party packages, and keep functions isolated to avoid conflicts.

## Common js vs Ecma Script

| Feature                     | CommonJS                        | ECMAScript Modules (ESM)       |
|-----------------------------|---------------------------------|--------------------------------|
| **Syntax**                  | `require()` and `module.exports`| `import` and `export`          |
| **Loading**                 | Synchronous (loads at runtime) | Asynchronous (can be dynamic)  |
| **File Extension**          | `.js`                           | `.mjs` (or `.js` if specified in `package.json`) |
| **Usage**                   | Node.js and older JS environments | Modern JS environments, Node.js (v12.17 and above) |
| **Default Exports**         | Single object as `module.exports`| `export default` for default exports |
| **Scope**                   | Local scope, not in strict mode | Strict mode enabled by default |
| **Node.js Support**         | Fully supported                 | Supported from Node.js v12.17+ |


## Module Caching


Module Caching in Node.js refers to the behavior where Node.js caches modules after they are first loaded, to prevent the overhead of reloading and re-executing the same module multiple times during the execution of an application.

### How Module Caching Works:

First Import: When you require() a module for the first time, Node.js loads and executes it, and then stores the result in memory.
Subsequent Imports: Any subsequent require() calls for the same module will return the cached version of the module, without re-executing its code.

### Benefits of Module Caching:

Performance: Avoids re-loading and re-executing the same module, improving performance.
State Persistence: Modules can maintain state between multiple imports, as they are executed only once.

## Semantic versioning

Semantic Versioning (SemVer) is a versioning scheme used to indicate the nature of changes in a software project through version numbers

1. MAJOR version (X.y.z):

- Incremented when there are breaking changes or backward-incompatible changes in the API or behavior of the software.
Example: If you remove or change an existing API method, the major version is increased.

2. MINOR version (x.Y.z):

- Incremented when new features or functionality are added in a backward-compatible manner.
Example: Adding new API methods, new optional features, or non-breaking improvements to the software.

3. PATCH version (x.y.Z):

- Incremented when there are backward-compatible bug fixes or minor improvements that do not change the public API or behavior.
Example: Fixing a bug, improving performance, or making small optimizations.


Helps developers and users understand the significance of a version change. Is it a major update, minor feature, or just a bug fix?


## What is a web server?

- It is a software which serves web content (HTML, PDF, web pages, api json)

- It uses HTTP protocol.

- When you type a URL in your browser or click on a link, the web server is what receives and processes that request, delivering the requested content, like web pages, images, or files, back to your browser.

- The default port for HTTP is port 80.

- For HTTPS (the secure version of HTTP), the default port is port 443.


## How web server works??

- Request Handling: When a client (usually a web browser) makes a request (for example, by entering a URL), the request is sent to the web server. (HTTP)

- Processing: The web server software processes this request. It might involve:

 1. Fetching a file from storage if it’s a static resource (like an image or HTML file).
 2. Running scripts or connecting to databases if it's a dynamic request (e.g., fetching user-specific data).

- Response: The server sends the processed data back to the client’s browser, displaying the requested page or data.

## Blocking single threaded web server

A blocking single-threaded web server handles requests one at a time in a single execution thread. This means that each request is processed sequentially: if one request takes time (e.g., for I/O operations like reading from disk or accessing a database), all other incoming requests must wait until that task completes. This behavior leads to "blocking" where other requests are held up, potentially resulting in poor performance, especially under high traffic.

- How It Works:

 1. Single Thread: The server runs on a single thread, meaning it can only handle one request at a time.

 2. Blocking Behavior: Each request blocks the thread until its operation (like data fetching or file reading) completes.
 
 3. Sequential Handling: Requests are queued and handled in sequence; a long request causes delays for subsequent requests.

## Problems with Blocking Single-Threaded Servers:

1. Poor Scalability: Blocking calls prevent handling other requests, limiting the server's capacity to handle multiple users simultaneously.

2. Slow Response Times: A single slow request can delay responses for all other requests.

3. Unresponsive Under Load: High-traffic scenarios can overwhelm the server, making it unresponsive or causing timeouts.


## Solution

Spin different web servers and put them behind a load balancer

- Solution: Asynchronous Non-Blocking I/O
To address these issues, servers can be designed to use asynchronous, non-blocking I/O. Node.js, for example, is single-threaded but designed around non-blocking I/O, allowing it to handle multiple requests efficiently in a single thread by not blocking on I/O operations.

## OTS Web server (Over-the-shelf)


An OTS (Off-the-Shelf) web server is a pre-built, general-purpose web server that can be readily used for hosting websites or applications without requiring extensive customization. These servers are designed to handle a wide range of use cases and are typically reliable, well-supported, and easy to set up and configure.

### Examples of OTS Web Servers:

1. Apache HTTP Server: One of the most widely used web servers, known for its robustness and modularity. It is open-source and suitable for a variety of applications.

2. Nginx: Known for its performance and ability to handle high loads, Nginx is often used as a web server or reverse proxy and is popular for serving static content efficiently.

3. Microsoft IIS (Internet Information Services): A web server developed by Microsoft, commonly used for hosting applications on Windows Server environments.

4. LiteSpeed: A high-performance server known for its speed and optimization, especially in shared hosting environments.

### Benefits of OTS Web Servers:

- Ease of Deployment: Set up is often straightforward, with ample documentation and pre-configured settings.

- Reliability: These servers are well-tested and secure, making them suitable for production environments.

- Community and Support: Widely used OTS web servers have extensive community support, documentation, and frequent updates.

- Modularity: Many OTS web servers support modules or plugins, allowing for flexibility in configuration and scaling.



### Use Cases:

OTS web servers are ideal for:

- Web Hosting Providers: They offer reliable, scalable solutions for shared hosting environments.

- Enterprises and Startups: Quickly deploy production-ready servers without significant development overhead.

- Developers and Small Businesses: Set up a reliable server without needing extensive technical expertise or resources.


##  HTTP


HTTP, or Hypertext Transfer Protocol, is the foundation of data communication on the web. It defines how messages are formatted and transmitted between web browsers (clients) and servers, allowing them to request and deliver web pages, images, and other resources. HTTP operates as a request-response protocol, where clients send requests to servers, which respond with the requested content or status codes.


HTTP requests and responses are the two main components of communication between a client (like a web browser) and a server on the web:

1. HTTP Request: This is sent by the client to request data or an action from the server. It includes:

Method: Specifies the action (e.g., GET, POST, PUT, DELETE).
URL: The resource address (e.g., /products).
Headers: Metadata like Content-Type or Authorization.
Body (optional): Data sent with the request, typically in POST and PUT requests.

2. HTTP Response: The server replies to the client’s request with this response, which includes:

Status Code: Indicates success or error (e.g., 200 OK, 404 Not Found).
Headers: Information about the response, like Content-Type.
Body: The actual content, such as HTML, JSON, or an error message.


## HTTP REQUEST
An HTTP request is a communication mechanism that allows a client (usually a web browser or app) to request resources or perform actions on a server. Here’s a breakdown:

1. Components of an HTTP Request
Request Line: Specifies the HTTP method, target URL (or resource), and HTTP version. Example: GET /index.html HTTP/1.1
Headers: Key-value pairs providing metadata about the request. Example:

Copy code
Host: www.example.com
User-Agent: Mozilla/5.0
Body: Contains data (optional, used in POST/PUT requests). Example:
json
Copy code
{
  "username": "JohnDoe",
  "password": "12345"
}

2. HTTP Methods
GET: Retrieve data.
POST: Submit data.
PUT: Update/replace data.
DELETE: Remove data.
HEAD: Similar to GET but only retrieves headers.
OPTIONS: Returns allowed methods for a resource.
PATCH: Partially updates a resource.

3. Request Flow
DNS Resolution: The domain (e.g., www.example.com) is resolved to an IP address.
Connection Establishment: A connection to the server is made (via TCP or TLS for HTTPS).
Request Sent: The client sends the request to the server.
Response Received: The server processes the request and sends back a response.


4. Common Headers
General Headers:
Host: Domain name of the server.
User-Agent: Client application making the request.
Content Headers:
Content-Type: Type of data in the body (e.g., application/json).
Content-Length: Size of the body.
Authorization Headers:
Authorization: Includes credentials for secure endpoints.
Caching Headers:
Cache-Control: Defines cache behavior.

5. Request Example
A POST request using curl:

bash
Copy code
curl -X POST https://api.example.com/login \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer TOKEN123" \
     -d '{"username": "JohnDoe", "password": "12345"}'

## HTTP Response

1. Components of an HTTP Response
A. Status Line
The first line of the response includes:

HTTP Version: Specifies the HTTP version (e.g., HTTP/1.1 or HTTP/2).
Status Code: Indicates the outcome of the request (e.g., 200 for success, 404 for not found).
Reason Phrase: A brief description of the status code

B. Response Headers
Headers provide metadata about the response. These are key-value pairs.

Examples:

yaml


Content-Type: text/html; charset=UTF-8
Content-Length: 1234
Date: Wed, 15 Nov 2024 10:00:00 GMT

C. Response Body
The response body contains the data requested by the client (e.g., HTML, JSON, or image). Not all responses include a body (e.g., 204 No Content).

2. HTTP Status Codes
Status codes are divided into five categories:



A. Informational (1xx)
Temporary responses used during request processing.

100 Continue: The server has received the request headers; the client should proceed with the body.


B. Success (2xx)
Indicates that the request was successful.

200 OK: The request succeeded, and the response body contains the data.
201 Created: A resource was successfully created.


C. Redirection (3xx)
The client must take additional actions to complete the request.

301 Moved Permanently: The requested resource has a new URL.
302 Found: Temporarily redirect to another URL.


D. Client Errors (4xx)
The request has an error from the client side.

400 Bad Request: The request was malformed.
401 Unauthorized: Authentication is required.
404 Not Found: The resource could not be found.


E. Server Errors (5xx)
The server encountered an error while processing the request.

500 Internal Server Error: General server error.
503 Service Unavailable: The server is temporarily unavailable.


3. Common Response Headers
A. General Headers
Date: Timestamp of when the response was generated.
Server: Information about the server (e.g., Apache, nginx).

B. Content Headers
Content-Type: Media type of the response body (e.g., application/json, text/html).
Content-Length: Size of the response body in bytes.

C. Caching Headers
Cache-Control: Instructions for caching (e.g., no-cache, max-age=3600).
ETag: Identifier for a specific version of the resource.

D. Security Headers
Strict-Transport-Security: Enforces HTTPS for future requests.
Content-Security-Policy: Controls resources that can be loaded by the browser.

4. Example HTTP Response
For a successful request:

makefile

HTTP/1.1 200 OK
Date: Wed, 15 Nov 2024 10:00:00 GMT
Server: Apache/2.4.41 (Ubuntu)
Content-Type: application/json
Content-Length: 123

{
   "message": "Request was successful",
   "data": {
      "id": 1,
      "name": "Example"
   }
}

5. Key Concepts
A. Persistent Connections
Modern HTTP uses persistent connections (HTTP/1.1+) by default, allowing multiple requests and responses over a single connection.

B. Chunked Responses
When the server doesn’t know the content size beforehand, it sends the response in chunks (using Transfer-Encoding: chunked).

C. Compression
Responses can be compressed for efficiency using headers like:

Content-Encoding: gzip
Content-Encoding: deflate


Understanding HTTP responses is critical for debugging, optimizing APIs, and ensuring effective client-server communication.

## HTTP APIS and routing

HTTP APIs (Application Programming Interfaces) allow clients to interact with servers using HTTP methods like GET, POST, PUT, and DELETE to access or manipulate resources. Routing defines how API endpoints (URLs) map to specific server logic or functions.



1. HTTP API Basics
A. Key Components
Endpoint: The URL path where the API is accessible (e.g., /users).
Method: The HTTP method determines the action to perform.
Request: Includes the HTTP method, headers, body (optional), and query parameters.
Response: The server's reply with a status code, headers, and a body.
B. Example
For a RESTful API managing users:

GET /users: Fetch a list of users.
POST /users: Add a new user.
PUT /users/1: Update user with ID 1.
DELETE /users/1: Delete user with ID 1.


2. Routing in APIs
A. What is Routing?
Routing is the process of defining URL paths and mapping them to specific server-side functions or handlers.

B. Types of Routes
Static Routes:

Match specific paths.
Example: /home, /about.
Dynamic Routes:

Include placeholders for parameters.
Example: /users/:id where :id is a dynamic value.
Catch-All Routes:

Handle unspecified or wildcard paths.
Example: /products/*.


## API Routing example
const express = require('express');
const app = express();

app.use(express.json()); // For parsing JSON bodies

// GET request to fetch users
app.get('/users', (req, res) => {
  res.json([{ id: 1, name: 'John Doe' }]);
});

// POST request to add a new user
app.post('/users', (req, res) => {
  const newUser = req.body;
  res.status(201).json({ message: 'User created', user: newUser });
});

// PUT request to update user by ID
app.put('/users/:id', (req, res) => {
  const userId = req.params.id;
  res.json({ message: `User ${userId} updated` });
});

// DELETE request to delete a user by ID
app.delete('/users/:id', (req, res) => {
  const userId = req.params.id;
  res.json({ message: `User ${userId} deleted` });
});

// Start the server
app.listen(3000, () => console.log('Server running on port 3000'));

## Parameterized URL
Parameterized URLs use dynamic placeholders (parameters) in the URL path or query string to handle variable data. These are common in APIs and routing systems for dynamically accessing or manipulating resources based on input values.

1. What Are Parameterized URLs?
A parameterized URL includes variables (parameters) marked with a special syntax like : or {}. These variables are replaced with actual values when the URL is used.

Example:

URL Template: /users/:id
URL with Parameter: /users/123 (where 123 is the id value)

2. Types of Parameters
A. Path Parameters
Embedded directly in the URL path.
Identified with :name or {name} syntax.

Example:
Template: /products/:productId
Actual: /products/42

B. Query Parameters
Passed after a ? in the URL.

Syntax: ?key=value&key2=value2.

Example:
URL: /products?category=books&sort=price