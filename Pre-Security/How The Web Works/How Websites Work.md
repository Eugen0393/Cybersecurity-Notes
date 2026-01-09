# 1. How Websites Work
When you visit a website, your browser (such as Safari or Google Chrome) sends a request to the web server, asking for information about the page you are visiting. The web server is simply a dedicated computer located somewhere else in the world that processes your requests.  
<img width="1272" height="396" alt="image" src="https://github.com/user-attachments/assets/31a13d2f-21a4-4e85-940f-11d4e1d8963b" />
## A website consists of two main components:

1. $\color{red}{\textsf{Front End}}$ (Client-Side) - this is how the website is displayed by your browser.
2. $\color{red}{\textsf{Back End}}$ (Server-Side) - this is the server that processes your request and returns a response.

# 2. HTML
## Websites are primarily created using the following tools:  
Hypertext Markup Language (HTML) is the language used to write websites. Elements (also known as tags) are the building blocks of HTML pages and instruct the browser how to display the content.  Below is an example:  
<img width="652" height="391" alt="image" src="https://github.com/user-attachments/assets/5595ae5a-783d-4b2b-9ae7-bcdaa5b05553" />  
The HTML structure (as shown in the screenshot) has the following components:

* The `<!DOCTYPE html>` defines that the page is a HTML5 document. This helps with standardisation across different browsers and tells the browser to use HTML5 to interpret the page.
* The `<html>` element is the root element of the HTML page - all other elements come after this element.
* The `<head>` element contains information about the page (such as the page title)
* The `<body>` element defines the HTML document's body; only content inside of the body is shown in the browser.
* The `<h1>` element defines a large heading
* The `<p>` element defines a paragraph
* There are many other elements (tags) used for different purposes. For example, there are tags for buttons (`<button>`), images (`<img>`), lists, and much more. 


Tags can contain attributes, such as the `class` attribute, which is used to style the element (for example, to change the color of the tag), or the `src` attribute, which is used for images to specify the location of the image: an element can have multiple attributes, each with its own unique purpose, for example, 
```
<p attribute="value1" attribute2="value2">. 

<p class="bold-text"><img src="img/cat.jpg">.
```  
# 3. JavaScript
JavaScript (JS) is one of the most popular programming languages ​​in the world, allowing you to create interactive web pages. HTML is used to create the structure and content of a website, while JavaScript is used to control the functionality of web pages.

# 4. Sensitive Data Exposure

`A confidential data leak occurs when a website fails to properly protect (or remove) sensitive information that is publicly accessible to the end user; this information is usually found in the website's source code. ` 

We now know that websites are built using many HTML elements (tags) that can be seen simply by "viewing the page source code." The website developer may have forgotten to remove login credentials, hidden links to private sections of the website, or other sensitive data displayed in HTML or JavaScript.

# 5. HTML Injection  
HTML Injection is a vulnerability that occurs when unfiltered user input is displayed on the page. If a website fails to sanitise user input (filter any "malicious" text that a user inputs into a website), and that input is used on the page, an attacker can inject HTML code into a vulnerable website.
