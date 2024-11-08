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

