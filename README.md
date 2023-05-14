<h1> 1)  What is non-blocking vs blocking? </h1>

<h3>Blocking is when the execution of additional JavaScript in the Node.js process must wait until a non-JavaScript operation completes. This happens because the event loop is unable to continue running JavaScript while a blocking operation is occurring.</h3>

<h2>// Example of Blocking (Synchronous)</h2>
<img src="https://github.com/masai-course/babariya_aniket_chetanbhai_fw21_1200/assets/112626195/c3976a9c-4d30-46ba-9d6b-5fd406f70802" alt="">


<h2>// Example of Non-Blocking (Asynchronous)</h2>
<img src="https://github.com/masai-course/babariya_aniket_chetanbhai_fw21_1200/assets/112626195/5de51ac4-79cd-4f64-a51e-a2b87cc4b508" alt="">

<br>

<h1>2) What is throughput? </h1>
<h3>Throughput is the rate at which data is processed or get transferred from one location to another location.
  It is measured in bits per second.
It is mainly used for measuring the performance of the network connection or the speed of hard drive and
RAM.
It may vary from device to device. It depends on various factors like your network connection, network
traffic as such.
</h3>

<br>

<h1>3) what is the difference between readFile and readFileSync? </h1>
<h3>
  readFile is non-blocking async.
  <br>
readFileSync is blocking sync.
  <br>
  
 In fs.readFile() method, we can read a file in a non-blocking asynchronous way, but in the fs.readFileSync() method, we can read files in a synchronous way, i.e. we are telling node.js to block other parallel processes and do the current file reading process. That is, when the fs.readFileSync() method is called the original node program stops executing, and the node waits for the fs.readFileSync() function to get executed, after getting the result of the method the remaining node program is executed.
</h3

<br>

<h1>4)How can you make a network request using http module? </h1>
  <h3>const http = require('http');
    <br>
    const server = http.createServer();
    <br>
    server.on('request', (request, response) => {
    <br>
  //Your code
    <br>
    });
  </h3>

<br>

<h1>5) How to create a web server without expresst? </h1>
 <h3>
   Yes, we can create web server without express. And It's Possible by using 'http'
   <br>
   const http = require('http');
    <br>
    const server = http.createServer();
    <br>
    server.on('request', (request, response) => {
    <br>
  //Your code
    <br>
    });
  </h3>
<br>

<h1>6) What is libuv? </h1>
  <h3>
    Libuv is a library written in the programming language C that helps nodejs to improve efficiency while running tasks parallelly. However, nodejs already have async API's. It uses Libuvs's thread pools if async API is not available in nodejs and processes are blocking the operations. Libuv doesn't perform the task itself, it only manages the operations.
<br>
    <br>
Consider that we have skills and potential to grow our careers. But we need a mentor to nurture it and we can utilize it well. So, The Libuv is a kind of mentor for nodejs.
    <br>
    <br>
    The event loop manages the operation and assigns the task according to machine specifications and operating system. And it is called event polling.
 <br>
    <br>
TCP and UDP sockets, and child processes are handles that keep the reference of callback. If handles are active, the Event loop allows the callback to run. Thread pools handle tasks in parallel that block I/O operations.
     <br>
    <br>
    In Libuv, the Event loop plays an important role to reduce the workload of the nodejs system. The event loop mainly has two parts: Event Queue and Threads
<br>
    <br>
The event loop listens to the event and adds events to the event queue. Then, The event loop assigns tasks to worker threads that handle the request.
It tracks the movement like the time to process the request, and whether an operation is completed or terminated.
Event loop continuously keeps checking the status of assigned tasks and adds/removes the event to the event queue as needed.
    <h3>

<br>

<h1>7) What are the different phases involved in event loop? </h1>
      <h3>
        The Event Loop consists of the six phases listed below, which are repeated as long as the application's code has to be executed: 
<br>
        <br>
1) Timers  <br>
2) I/O Callbacks  <br>
3) Waiting / Preparation  <br>
4) I/O Polling  <br>
5) setImmediate() callbacks  <br>
6) Close events  <br>
      </h3>
<br>


<h1>8) What are timers in Node.js? </h1>
      <h3>
      The core timers module in Node.js provides timers, or functions that perform callbacks after a given amount of time. setTimeout() and setInterval() are two global functions provided by this module (). These let you to define code that will run once a certain amount of time has passed. 
<br>
        <br>
The Event Loop executes the timers phase directly. The Event Loop changes its own time at the start of this phase. The timers are then checked in a queue or pool. All timers that are currently set are in this queue. The Event Loop compares the timer with the least wait time to the current time of the Event Loop. The timer's callback is scheduled to be triggered once the call stack is empty if the wait time has expired. 
<br>
        <br>
There are two types of timers in Node.js: setTimeout() and setInterval() (). The main difference is that setInterval() has a repeat flag, which returns the timer to the queue once it has completed its execution. </h3>
<br>

<h1>9) What is NVM? how do you use it? </h1>
      <h3>
      Node Version Manager (NVM), as the name implies, is a tool for managing Node versions on your device. Different projects on your device may be using different versions of Node. Using only one version (the one installed by npm ) for these different projects may not give you accurate execution results.
        <br>
      <br>
       to use NVM , <br>
Run the nvm use command, followed by the version number of Node you want to use (e.g. nvm use 16.9. 1 ) to use a specific version. Alternatively, you can use use latest , lts , or newest instead of a specific version number, where newest is the latest installed version.
      </h3>
    
<br>

<h1>10) What is common.js? how is it different from es modules? </h1>
<h3>
  CommonJS is a module formatting system. It is a standard for structuring and organizing JavaScript code. CJS assists in the server-side development of apps and it’s format has heavily influenced NodeJS’s module management.
  <br>
  <br>
  In Node.js each of the JavaScript files is handled as an individual separate CommonJS module. This infers that the variables, functions, classes, etc., which are present inside of it, are not, by default, directly accessible to other files. We need to explicitly describe the module system as to which parts of the code should be exported and which not. CommonJS modules are the original way to package JavaScript code for Node.js. 
<br>
  <br>
  
  This loading paradigm was designed with server-side JavaScript in mind and is not suitable for client-side applications. Modules are loaded synchronously and are accessed in the same order that JavaScript locates them. 
<br>
  <br>
Symbols that are defined inside a JavaScript file are considered modules when they are exported. It could be variables, functions, objects, classes, etc. Let us take an example of string manipulation JavaScript file stringOps.js, which has several functions, like one to remove all spaces from the string.
  <br>
  <br>
Ok… So, what is a module? A module is just a bit of code encapsulated in a file, and exported to another file. Modules focus on a single part of functionality and remain loosely coupled with other filed in an application. This is because there are no global or shared variables between modules, as they only communicate via the module.exports object. Any code that you want to be accessible in another file can be a module!
      </h3>
     
 <h2>CommonJS VS ES Modules</h2>
      
  <h3>
  CommonJS vs ES Modules: Functionality  <br>
CommonJS modules are similar to ES modules, but there are a few key differences. First, CommonJS modules must be loaded from a module repository, such as npm.
 <br> 
Second, CommonJS modules can only be accessed from within the context of a Node.js application. CommonJS modules do not have exports or prototypes like ES modules do. Finally, the require() function in CommonJS is not equivalent to the import() function in ES Modules.
 <br> <br>
CommonJS vs ES Modules: Compilation  <br>
CommonJS is a module system inspired by the AMD API from Microsoft. It allows modules to be written in a similar way to AMD modules, with the main difference being that CommonJS modules can be loaded into any node.js environment.
 <br>
ES Modules are a new module system developed by Google which allows for greater modularity and reuse across different programming languages. The advantage of using ES Modules is that they can be compiled into native code which makes them faster and more efficient than CommonJS modules.
 <br> <br>
CommonJS vs ES Modules: Dependencies  <br>
CommonJS modules are AMD-compliant and can be used in both Node.js and browsers. ES modules are not AMD-compliant but are supported in browsers through the webpack module loader.
 <br>
CommonJS modules have a few dependencies that must be installed before they can be used: nodejs, npm, and yeoman. These dependencies can be installed using the following commands:
 <br>
npm install -g nodejs npm install -g npm yeoman 
 <br>
ES modules do not have any dependencies other than the module loader itself. However, some development tools may require additional libraries, such as Babel. To install these tools, you can use the following command: 
 <br>
yarn add babel babel-cli babel-preset-env
 <br> <br>
CommonJS vs ES Modules: Typescript  <br>
CommonJS modules are a popular way to modularize JavaScript code. They allow you to export and import modules using the export and import keywords, respectively.
 <br>
ES Modules are a newer way to modularize JavaScript code. Unlike CommonJS modules, which rely on exports and imports, ES Modules use the module keyword. This allows you to define modules in a more declarative way without having to use the export and import keywords. Enroll in Full Stack online course to learn the essential modules in node js.
 <br> <br>
CommonJS vs ES Modules: File Structure  <br>
The main difference between CommonJS and ES modules is the file structure. With CommonJS, all of the dependencies for a project are stored in one file called node_modules/. With ES modules, each dependency is stored in its files. This allows developers to better control how their dependencies are used and makes it easier to version software.
 <br> <br>
CommonJS vs ES Modules: Export  <br>
CommonJS modules are a popular and efficient way to modularize code. They use the export keyword to make functions and variables accessible from other modules.
 <br>
ES modules are a newer version of the CommonJS module format. They use the export keyword but also include a require() function that automates the process of including other ES modules in your project.
 <br> <br>
CommonJS vs ES Modules: Import  <br>
ES modules provide a way to group related code together for reuse. CommonJS, on the other hand, lets you use any module from the global namespace.
 <br>
To answer your question about CommonJS or ES modules which is better, CommonJS modules are typically used in Node.js applications, as they allow for a more centralized approach to code management and require no additional configuration on the part of the developer. 
 <br>
ES modules are popular in browser-based applications because they can be loaded asynchronously and don't require an underlying runtime environment like Node.js.
      </h3>
<br>

<h1>11) How does the crypto module work? </h1>
      <h3>
      The Node.js crypto module provides cryptographic functions to help you secure your Node.js app. It includes a set of wrappers for OpenSSL’s hash, HMAC, cipher, decipher, sign, and verify functions.
<br>
        <br>
crypto is built into Node.js, so it doesn’t require rigorous implementation process and configurations. Unlike other modules, you don’t need to install Crypto before you use it in your Node.js application.
<br>
        <br>
crypto allows you to hash plain texts before storing them in the database. For this, you have a hash class that can create fixed length, deterministic, collision-resistant, and unidirectional hashes. For hashed data, a password cannot be decrypted with a predetermined key, unlike encrypted data. An HMAC class is responsible for Hash-based Message Authentication Code, which hashes both key and values to create a single final hash.
      </h3>
     
<h2> The mechanism in Cryptography:</h2> 
<h3>
Hashing: This is a mechanism to convert a plain text to ciphertext. It is a one-way cryptographic function i.e, we can’t convert cipher text to plain text. It is widely used in authentication systems to avoid storing plain text passwords in databases but is also used to validate files, documents, and other types of data.  Message Digest 5(MD5), RSA, SHA, etc are Widely used algorithms for hashing.
<br>
      <br>
Encryption and Decryption: Encryption algorithms take input and a secret key and generate a random-looking output called a ciphertext. This operation is reversible. Decryption is the reverse of encryption. This algorithm takes the same secret key and ciphertext and it returns back our original plain text. This is widely used in messaging systems like WhatsApp etc.  AES, etc are Widely used algorithms for encryption and decryption.
      </h3>
<h2>Features of Crypto in Node.js:  </h2>
<h3>
1) It’s easy to get started <br>
2) A lot of widely used algorithms are there with different versions<br>
3) The source code is cleaner and consistent.<br>
4) It uses JavaScript everywhere so you can use it with node.js
      </h3>  

<br>

<h1>12) What are web sockets? </h1>
<h3>
WebSocket is a communications protocol for a persistent, bi-directional, full duplex TCP connection from a user's web browser to a server. A WebSocket connection is initiated by sending a WebSocket handshake request from a browser's HTTP connection to a server to upgrade the connection.
  <br>
  <br>
The WebSocket API is an advanced technology that makes it possible to open a two-way interactive communication session between the user's browser and a server. With this API, you can send messages to a server and receive event-driven responses without having to poll the server for a reply.
      </h3>
<br>

<h1>13) What are microservices? </h1>
      <h3>
These microservices are architecture patterns that allow applications to be built of collections of several smaller units. In this blog, our DEVIT Engineers will investigate microservices and show how to implement them into your React and Node.js applications and websites.
        <br>
        <br>
        In a microservice, each software application feature is separated from the other, in most cases with their respective servers and databases. Applications built with this kind of architecture are loosely coupled, also referred to as distributed applications.
      </h3>
<br>

<h1>14) Creating a CLI based app using Node.js and publish it </h1>

<br>

<h1>15) How does express work? </h1>
<h3>
  Express is a node js web application framework that provides broad features for building web and mobile applications. It is used to build a single page, multipage, and hybrid web application. It's a layer built on the top of the Node js that helps manage servers and routes.
  <br>
  <br>
app. get() is a function that tells the server what to do when a get request at the given route is called. It has a callback function (req, res) that listen to the incoming request req object and respond accordingly using res response object. Both req and res are made available to us by the Express framework.     
 </h3>
<br>

<h1>16) What are routes? </h1>
      <h3>
         Routing refers to determining how an application responds to a client request to a particular endpoint, which is a URI (or path) and a specific HTTP request method (GET, POST, and so on). In simple terms, Routing allows targeting different routes or different URLs on our page
        <br><br>
      Whenever a client enters the URL of the website in the browser, an HTTP request is generated, and in return, an HTTP Response is generated and the web page or the website is rendered to the client. These HTTP requests are sent to the backend server, which then responds to the request.The point to note is how the server will know which page is to be rendered corresponding to each request.
        <br><br>
        Here Routing comes to Picture, Routing refers to determining how an application responds to a client request to a particular endpoint, which is a URI (or path) and a specific HTTP request method (GET, POST, and so on). In simple terms, Routing allows targeting different routes or different URLs on our page.
      </h3>
<br>

<h1>17)What are Middlewares? </h1>
      <h3>
        The middleware in node. js is a function that will have all the access for requesting an object, responding to an object, and moving to the next middleware function in the application request-response cycle.
        <br><br>
        A request handler with access to the application's request-response cycle is known as middleware. It's a function that holds the request object, the response object, and the middleware function. Middleware can also send the response to the server before the request.
      </h3>
      <h2>From given code you can pass data from one middleware to other</h2>
      <img src="https://github.com/masai-course/babariya_aniket_chetanbhai_fw21_1200/assets/112626195/6a3e3a63-9bf5-4dd9-adcc-6d8bd6c447e2">

<br>

<h1>18) What is MVC framework? </h1>
<h3>
      MVC stands for Model, View, Controller is an architectural pattern that separates an application into three main logical components: the model, the view, and the controller. Each one of these components is built to handle specific development aspects of an application.
 <br>
   <br>
Model is the database interface which lets you interact with the database API and create different entity schemas of your app on the database (MySQL, MongoDB), it gets called from controller depending on the client’s request if it needs a stored data then the controller will ask the model interface for providing it with the needed data.<br><br>
  View is what compiles and renders into plain HTML and what the client in most cases going to get back as a response of what he requested (for ex: to view his profile details), the view needs to use a Template Engine for doing the rendering process where the controller feed it with needed data (data from database and client) and the view renders and convert everything into plain HTML that the browser could understand and display.<br><br>
   Controlleris the part that takes care of client request processing which handles the HTTP Request and returns a response the response could be either a JSON if you’re calling an API endpoint or regular HTML webpage.
       </h3>
<br>

<h1>19) How do you do validations? </h1>
<h3>
  Validation in node.js can be easily done by using the express-validator module. This module is popular for data validation. There are other modules available in market like hapi/joi, etc but express-validator is widely used and popular among them.
  <br><br>
  Here is the code for validation
</h3>
      <br>
      <img src="https://github.com/masai-course/babariya_aniket_chetanbhai_fw21_1200/assets/112626195/672d1386-6fc4-47f1-8b82-950f9646365d">
<br>

<h1>20)  How do you do static routing? </h1>
<h3>
  Static Routing is that kind of routing where we to set a router manually for a specific route. There are some demerits of it like everytime if we have a new file then we have set route for that file manually. And also it’s hard to handle the route for every file in our project.
  <br><br>
  step 1: Create one server
  <br><br>
  step 2: we created our server so we need fs package. Then we have to take the benefit of Node JS request object that contains two special property i.e url and method. The request.method gave us the method of the request and request.url will give us the browser’s request URL that the browser requested for. Now it’s time to check for the URL and method and serve the static pages.
      </h3>
      <br>
      <img src="https://github.com/masai-course/babariya_aniket_chetanbhai_fw21_1200/assets/112626195/6933dec7-cfb2-432a-83d5-18f0e0a2df4b">
      <br>
      <h2>
        And follow the above same steps and every time just change the case and read the file for that specific kind and just change the header every time.
      </h2>
       <br>
      <img src="https://github.com/masai-course/babariya_aniket_chetanbhai_fw21_1200/assets/112626195/8afb45ea-7c2a-4378-8917-802763786ac1">
      

<br>

<h1>21) What are some templating engines? </h1>
      <h3>
       1) Jade <br>
2) Vash<br>
3) EJS<br>
4) Mustache<br>
5) Dust.js<br>
6) Nunjucks<br>
7) Handlebars<br>
8) atpl<br>
9) haml<br>
        <br>
       // Advantages of Template engine in Node.js<br>
        <br>
1)Improves developer's productivity.<br>
2)Improves readability and maintainability.<br>
3)Faster performance.<br>
4)Maximizes client side processing.<br>
5)Single template for multiple pages.<br>
6)Templates can be accessed from CDN (Content Delivery Network).<br>
      </h3>

<br>

<h1>22) How do you manage sessions in express? </h1>
      <h3>
      Session management can be done in node.js by using the express-session module. It helps in saving the data in the key-value form. In this module, the session data is not saved in the cookie itself, just the session ID.
      </h3>
      <br>
      <img src="https://github.com/masai-course/babariya_aniket_chetanbhai_fw21_1200/assets/112626195/6ca65884-c9a7-4534-8afa-81fcd976102f">
      <br>
<br>

<h1>23) How do you manage cookies with express? </h1>
      <h3>
        Cookies are simple, small files/data that are sent to client with a server request and stored on the client side. Every time the user loads the website back, this cookie is sent with the request. This helps us keep track of the user’s actions.
<br>
The following are the numerous uses of the HTTP Cookies −
<br>
1) Session management<br>
2) Personalization(Recommendation systems)>br>
3) User tracking<br>
      </h3>
        <br>
      <img src="https://github.com/masai-course/babariya_aniket_chetanbhai_fw21_1200/assets/112626195/9f322cc8-9c3e-4b07-8426-e0c38c096737">
      <br>
        <br>
      <img src="https://github.com/masai-course/babariya_aniket_chetanbhai_fw21_1200/assets/112626195/632374b3-4673-46e2-a093-791bc7460529">
      <br>


<h1>24) What are common libraries you work with express? </h1>
<h3>
  These are some common libraries we work with express,<br><br>
  1) Cors<br>
  2) Nodemon<br>
  3) Mongoose<br>
  4) dotenv<br>
  5) Bcrypt<br>
  6) Jsonwebtoken<br>
  7) Socket.io<br>
  8) typescript<br>
  </h3>
<br>

<h1>25)What is CORS? </h1>
      <h3>
      Cross-Origin Resource Sharing (CORS) is an HTTP-header based mechanism that allows a server to indicate any origins (domain, scheme, or port) other than its own from which a browser should permit loading resources. CORS also relies on a mechanism by which browsers make a "preflight" request to the server hosting the cross-origin resource, in order to check that the server will permit the actual request. In that preflight, the browser sends headers that indicate the HTTP method and headers that will be used in the actual request.
          <br><br>
      For security reasons, browsers restrict cross-origin HTTP requests initiated from scripts. For example, XMLHttpRequest and the Fetch API follow the same-origin policy. This means that a web application using those APIs can only request resources from the same origin the application was loaded from unless the response from other origins includes the right CORS headers.
      </h3>
    
<br>

<h1>26) What is testing?</h1>
      <h3>
        With any application, testing is an integral part of the development process. For example, testing allows you to verify that changes to a project don’t break its expected behavior, and tests can act as pseudo documentation when path flows are documented.
        <br><br>
        When testing with Node.js, you’ll typically use either Mocha, Chai, Jest, Chai HTTP, or Sinon. We’ll review these later. First, there are several different types of tests that we should be familiar with.
      </h3>
<br>

<h1>27) What is unit testing? </h1>
<h3>nit testing is important to verify the behavior of the smallest units of code in your application. It helps improve the quality of your code and reduces the amount of time and money you spend on bug fixing. Moreover, unit testing helps you find bugs early on in the development life cycle and increases your confidence in the code. This post we’ll show you how to get started with Node.js unit testing in practice, with examples. Think of this post as a “hello world” for unit testing in Node.js.
      <br>
  <br>
  Unit testing involves testing your application’s code and logic, which includes anything that your application can do on its own without having to rely on external services or data
      </h3>
<br>

<h1>28)What is functional testing? </h1>

<br>

<h1>29)What is HTTPS? what is the difference between HTTP and HTTPS? </h1>
      <h3>
        Hypertext transfer protocol secure (HTTPS) is the secure version of HTTP, which is the primary protocol used to send data between a web browser and a website. HTTPS is encrypted in order to increase security of data transfer. This is particularly important when users transmit sensitive data, such as by logging into a bank account, email service, or health insurance provider.
<br><br>
Any website, especially those that require login credentials, should use HTTPS. In modern web browsers such as Chrome, websites that do not use HTTPS are marked differently than those that are. Look for a padlock in the URL bar to signify the webpage is secure. Web browsers take HTTPS seriously; Google Chrome and other browsers flag all non-HTTPS websites as not secure.
        <br><br>
        HTTPS is HTTP with encryption and verification. The only difference between the two protocols is that HTTPS uses TLS (SSL) to encrypt normal HTTP requests and responses, and to digitally sign those requests and responses. As a result, HTTPS is far more secure than HTTP. A website that uses HTTP has http:// in its URL, while a website that uses HTTPS has https://.
      </h3>
<br>

<h1>30) What is SSL/TLS?</h1>
      <h3>
      The node:tls module provides an implementation of the Transport Layer Security (TLS) and Secure Socket Layer (SSL) protocols that is built on top of OpenSSL.
      <br>
        <br>
        SSL/TLS encrypts communications between a client and server, primarily web browsers and web sites/applications. SSL (Secure Sockets Layer) encryption, and its more modern and secure replacement, TLS (Transport Layer Security) encryption, protect data sent over the internet or a computer network.
        <br><br>
        It is used to execute JavaScript codes outside or without a browser
      </h3>
<br>

<h1>31)What is OWASP? </h1>
<h3>OWASP stands for Open Web Application Security Project. It's a comprehensive online source of documentation and tools for web security.
      <br><br>
The Open Web Application Security Project (OWASP) is a non-profit organization founded in 2001, with the goal of helping website owners and security experts protect web applications from cyber attacks. OWASP has 32,000 volunteers around the world who perform security assessments and research.
      </h3>
<br>

<h1>32)What is the difference between SQL and NoSQL databases?</h1>
      <h3>
        # SQL databases are relational, and NoSQL databases are non-relational.<br>
# SQL databases use structured query language (SQL) and have a predefined schema. NoSQL databases have dynamic schemas for unstructured data.<br>
# SQL databases are vertically scalable, while NoSQL databases are horizontally scalable.<br>
# SQL databases are table-based, while NoSQL databases are document, key-value, graph, or wide-column stores.<br>
# SQL databases are better for multi-row transactions, while NoSQL is better for unstructured data like documents or JSON<br>
      </h3>
<br>

<h1>33)What are some common queries in SQL?</h1>
      <h3>
1. Joining Values from Text Columns in One String<br>
2. Identify Values Aligning with Specific Pattern<br>
3. Mathematical Operators<br>
4. Using Aliases of Tables and Columns<br>
5. Determining Average of Values in a Column<br>
6. Counting Number of Rows<br>
7. Determine Sum of Values in Columns<br>
8. Find Intersection of Data Sets<br>
9. Addition of Data from Various Tables<br>
10. Identifying Maximum Value in a Column<br>
      </h3>
<br>

<h1>34)How do you do joins in SQL?</h1>
<h3>
  SELECT Orders.OrderID, Customers.CustomerName, Orders.OrderDate<br>
FROM Orders<br>
INNER JOIN Customers ON Orders.CustomerID=Customers.CustomerID;<br>
      </h3>
<br>

<h1>35)How do you use lookup in mongodb?</h1>
<h3>
  {<br>
   $lookup:<br>
     {<br>
       from: "collection to join",<br>
       localField: "field from the input documents",<br>
       foreignField: "field from the documents of the "from" collection",<br>
       as: "output array field"<br>
     }<br>
}
  </h3>
<br>

<h1>36)What is CAP theorem?</h1>
<h3
If a node in the system goes down, things will keep working as expected (also known as fault-tolerance). The CAP theorem is largely based on the assumption that network failures are inevitable and will always occur. When such partitions occur, you must choose between either consistency or availability.</h3>
<br>

<h1>37)What is indexing?</h1>
<h3>Indexes are data structures that support the efficient execution of queries in MongoDB. They contain copies of parts of the data in documents to make queries more efficient. Without indexes, MongoDB must scan every document in a collection to find the documents that match each query.</h3>
<br>

<h1>38)What is DB replication?</h1>
  <h3>
 Database replication is the process of creating copies of a database and storing them across various on-premises or cloud destinations. It improves data availability and accessibility. Every user connected to the system can access copies of the same (up-to-date) data.<br><br>
    How database replication works?<br>
Database replication can either be a single occurrence or an ongoing process. It involves all data sources in an organization's distributed infrastructure. The organization's distributed management system is used to replicate and properly distribute the data amongst all the sources.
<br><br>
Overall, distributed database management systems (DDBMS) work to ensure that changes, additions and deletions performed on the data at any given location are automatically reflected in the data stored at all the other locations. DDBMS is essentially the name of the infrastructure that allows or carries out database replication -- the system that manages the distributed database, which is the product of database replication.
  </h3>
<br>

<h1>39)What is PACELC?</h1>
  <h3>
    The PACELC theorem is an extension to the CAP theorem. Both theorems were developed to provide a framework for comparing distributed systems. Like the CAP theorem, the PACELC theorem states that in case of network partitioning (P) in a distributed computer system, one has to choose between availability (A) and consistency (C). PACELC extends the CAP theorem by introducing latency and consistency as additional attributes of distributed systems. The theorem states that, “else (E), even when the system is running normally in the absence of partitions, one has to choose between latency (L) and consistency (C).”
<br><br>
CAP theorem was originally formulated by a noted computer scientist, Eric Brewer. The theorem states that it is impossible for a distributed system to provide more than two of the following three guarantees:
<br>
Consistency – the same response is given to all identical requests<br>
Availability – access continues even during a partial system failure<br>
Partition Tolerance – operations remain intact even when some nodes are unavailable.<br><br>
PACELC was developed to address a key limitation of the CAP theorem: it makes no provision for performance or latency. For example, according to the CAP theorem, a database can be considered Available if a query returns a response after 30 days. Obviously, such latency would be unacceptable for any real-world application.
  </h3>
<br>

<h1>40)What is Normalization / Denormalization?</h1>
<h3>
 ** Normalization**: Normalization is the method used in a database to reduce the data redundancy and data inconsistency from the table. It is the technique in which Non-redundancy and consistency data are stored in the set schema. By using normalization the number of tables is increased instead of decreased.
<br><br>
**Denormalization**: Denormalization is also the method which is used in a database. It is used to add the redundancy to execute the query quickly. It is a technique in which data are combined to execute the query quickly. By using denormalization the number of tables is decreased which oppose to the normalization.
  </h3>
  <br>
  <img src="https://github.com/masai-course/babariya_aniket_chetanbhai_fw21_1200/assets/112626195/5d53941f-1e8b-40b1-a725-e4169191dc7f">
  <br>

<h1>41)What is Entity Relationship Model? ( ER Model )</h1>
      
      <h3>
      
An entity relationship diagram (ERD), also known as an entity relationship model, is a graphical representation that depicts relationships among people, objects, places, concepts or events within an information technology (IT) system.
      </h3>
