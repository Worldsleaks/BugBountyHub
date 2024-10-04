# Web Browsers

Web browsers act as an interface to access web applications and are responsible for interpreting and displaying content to the end user. They are primarily responsible for rendering pages by processing HTML, CSS and JavaScript.

In the context of the ever-evolving web security landscape, web browsers have expanded their role beyond just rendering pages and continuously introducing security controls to protect the privacy and security of the users.

The following squeme gives a high-level overview of core browser components:

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1).png" alt=""><figcaption><p>High-level overview of a browser's internals</p></figcaption></figure>

### 1. User Interface

This represents the HTML and CSS and displays the parsed content on the screen. The UI is designed to provide intuitive control over browser functionality, enabling users to manage web pages, perform searches, and configure browser preferences.

### 2. Browser Engine

Serves as a bridge between the User Interface (UI) and the Rendering Engine in a web browser. Its primary role is to handle actions initiated by the user through the UI, such as navigating to a URL or refreshing a page, and then communicating those requests to the Rendering Engine for processing.

### 3. Rendering Engine

The **Rendering Engine** is responsible for transforming the web content (HTML, CSS, and JavaScript) into a visual representation that users can interact with on their screen.&#x20;

When a browser fetches a web page, the rendering engine parses the HTML and builds the Document Object Model (DOM) tree, processes CSS to apply styling rules, and then combines the structure and styles to create the render tree.

Engines used by the most common web browsers:

| Browser | Engine |
| ------- | ------ |
| Chrome  | Blink  |
| Firefox | Gecko  |
| Safari  | WebKit |

### 4. Networking

The **Networking** component of a browser is responsible for handling all network-related tasks, such as making HTTP/HTTPS requests to fetch web content, managing data transmission, and ensuring secure communication between the browser and remote servers.

### 5. JavaScript Interpreter

The **JavaScript Interpreter** is the component of a web browser responsible for executing JavaScript code on web pages.

### 6. UI Backend

The **UI Backend** in a web browser is the component responsible for drawing and rendering the basic graphical elements of the browser's user interface, such as buttons, menus, and windows. It works alongside the browser's rendering engine but focuses on non-webpage elements that are part of the browser itself, including the address bar, tabs, scrollbars, and dialog boxes.

### 7. Data Storage

This component is responsible for storing data on the client side. This includes mechanisms such as cookies, Web Storage, IndexedDB, WebSQL and FileSystem.

