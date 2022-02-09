# introToReact
Introduction to the React Library
React is a declarative and component-based JavaScript library.

Declarative means that React updates the application interface when data changes. As an example of this declarative functionality, it is utilized when a user logs into their account and their name displays elsewhere on the screen.

Component-based design is the concept of writing small bits of functionality that are reusable throughout an application. For example, a log-in form could be a component that is displayed in multiple places or situations. Component-based design improves the development and maintenance of large codebases. You will learn more about it later this week.

Before you start using React, it is important to understand the role of frameworks and libraries in web development.
What Is A Framework?
A framework is a collection of tools and features built into a language that attempts to save a developer time by automating the mundane tasks they would normally have to complete manually. Angular (Links to an external site.) is a front-end framework that includes built-in functionality and a computer-line interface tool. Angular is opinionated, meaning that it enforces the developer to follow a specific folder structure and development practices.

For example, suppose you are developing a user input form. If you are using a framework like Angular, you will have to use specific, built-in form functionality to create it. A library, on the other hand, will allow you to create the form with more flexibility.

What Is A Library?
A library is an unopinionated collection of prewritten code. Unopinionated means that it offers flexibility and freedom when developing an application. React is a JavaScript library that has no one specific folder structure that you must follow and no built-in functionality for things like routing, forms, or network calls. Instead, the developer must decide how they will structure their project and what packages they will use.

When To Use A Framework Vs. A Library
Frameworks and libraries have advantages and disadvantages. Both options are widely used in the software development industry, and it is good to be familiar with them. You should choose what you use based on the needs of your project and your personal preferences.

Advantages	Disadvantages	Examples
Framework	You can develop an application quickly without making decisions upfront.	You have less flexibility in how your application operates and what tools you can use.	Angular, Next.js, Redwood.js, Vue
Library	You have complete control over the codebase and the flexibility to use several packages and tools within your application.	You have to create the application manually and make several decisions, which will take longer.	React
In this course, you will learn how to use the React library and how to make decisions about the development of your application. After you learn how to leverage the library, if you want to add the framework functionality, you can use frameworks that are based on React (e.g., Next.js (Links to an external site.), Gatsby (Links to an external site.), and Redwood.js (Links to an external site.)).

# What is JSX?
JSX  (Links to an external site.)is a JavaScript syntax extension that allows HTML-like code to be written in JavaScript. With JSX, you can put HTML-like syntax inside of JavaScript code to render an HTML element and give it functionality.

Unlike Angular and Vue, which use HTML templates, React uses JSX to combine the UI code and logic in one place.

Introduction To JSX Syntax
Review the example of JSX below:

const title = 'Hello World';

const element = <h1>{title}</h1>;
Notice how the <h1> elements and reference to the title variable are assigned to the element variable. In this example of JSX, the HTML elements are assigned to a JavaScript variable.

If the element variable was rendered by React, the web page would display the text “Hello World” in h1 (header) tags.
