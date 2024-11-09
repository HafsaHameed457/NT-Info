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