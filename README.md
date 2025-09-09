# Building a Basic Chatbot Using ChatGPT

## Pre-requisites

### Understanding the basics of Node.js and Express.js

Node and Express are two technologies that are commonly used to create web applications.

- **Node.js** is a runtime environment that allows you to run JavaScript code on the server side, without a browser.
- **Express.js** is a framework that provides a set of features and tools to simplify the development of web applications with Node.js.

Some of the benefits of using Node and Express are:

- They are fast and scalable, as they use an event-driven, non-blocking I/O model that can handle many concurrent requests.
- They are flexible and modular, as they allow you to use various libraries and middleware to customize your application according to your needs.
- They are easy to learn and use, as they are based on JavaScript, which is a popular and widely used programming language.

## Task 1: Set Up Your Project

Here, we are setting up a Node.js project using the Express.js framework. Node.js is a JavaScript runtime that allows you to run JavaScript on the server, while Express.js is a web application framework for Node.js.

Follow the below instructions and refer to the screenshots for creating a Node.js Project.

**Step 1:** Open a terminal, click on "Terminal", and then select the "New Terminal" option.

**Step 2:** Create a new directory for your project named `software-dev-chatbot`, navigate to the directory, and initialize a Node.js project using the commands below.

```bash
mkdir software-dev-chatbot
cd software-dev-chatbot
npm init -y
```

**Step 3:** Install express and openai dependencies by executing the following command.

```bash
npm install express openai
```

**Step 4:** Create a new directory named public inside a project directory using the below command.

```bash
mkdir public
```

## Task 2: Create the user interface for your chatbot using HTML and CSS

Create an `index.html` file within the public directory, right-click on the public folder, and select the "New File" option, as shown in the screenshot below. This file will function as the user interface for your chatbot.

Inside the HTML file, we are using the following elements:

- **Text input element** → To take user input
- **Submit button** → To submit the question from the user
- **Text area** → Where the chatbot's responses will be displayed

### Here are the steps to set a chatbot logo of your choice:

1. Download an image from the internet for the chatbot logo and name it `chat.png`
2. Right-click on the public folder, and select the "Upload Files" option, as shown in the screenshot below
3. Choose the downloaded image and click "OK" to upload it

The styling is applied through an external CSS file (`style.css`).

The implementation of chatbot logic is done through an external JavaScript file named `main.js`.

You can type a message, and click the Send button, to interact with the chatbot.

Create a `style.css` file in the public directory.

## Task 3: Create a JavaScript file to implement the functionality of the Chatbot

Create a `main.js` file in the public directory to implement the functionality.

In the `main.js` file, the JavaScript code is designed to handle user input and initiate an API call to the OpenAI API.

- An event listener is attached to the submit button so that when the user clicks it, the code is executed.
- In the event listener callback function, we retrieve the user's input from the text input element and display their message in the chat log.
- Next, we make an API request to the server with the user's message using the `fetch()` function, specifying the appropriate endpoint on the server to receive this request.
- After receiving the response from the OpenAI API, we send it back to the client and display the chatbot's response in the text area of the `index.html` file.
- We then append the response to the chat log on the front end, making the conversation visible on the UI (User Interface).

## Task 4: Create an Express Server and integrate OpenAI API

Create a new file named `server.js` within your project directory (`software-dev-chatbot`).

This file will be responsible for managing API requests and integrating with OpenAI.

This code sets up a basic Express.js server that serves static files from a public directory.

- It includes a route for the root path ('/') to serve an HTML file.
- Additionally, there is a POST endpoint `/getChatbotResponse` that receives a user message, utilizes an OpenAI API wrapper (OpenAIAPI), generates a chatbot response using the OpenAI API, and sends the response back to the client.
- The server listens on a specified port 3000, and a message is logged to the console when the server is successfully running.

## Task 5: Create OpenAI API Module

Create an `openai.js` file within the project directory to encapsulate the OpenAI API logic.

This code facilitates communication with the OpenAI API, specifically the gpt-3.5-turbo Codex engine, allowing developers to generate responses based on user input through a secure configuration using an API key.

## Task 6: Run Your Application

**Step 1:** Run your Express server by executing the below command in the Terminal

```bash
node server.js
```

**Step 2:** Click on the "Skills Network" button on the left, which will open the "Skills Network Toolbox"

**Step 3:** When you enter a question and click Send, the chatbot will respond to your question using the OpenAI API.

**Step 4:** You can submit the following software development-related questions one at a time to the chatbot by entering them in the "Ask me anything" text box.

Click Send to receive a response from the chatbot.

### Sample Questions:

- **Q1:** What is the difference between a compiler and an interpreter?
- **Q2:** What is the difference between a stack and a queue?
- **Q3:** What is the difference between a linked list and an array?