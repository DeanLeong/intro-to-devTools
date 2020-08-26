![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) **SOFTWARE ENGINEERING IMMERSIVE**

# Intro To React Dev Tools

![](https://media.giphy.com/media/10eJOwQ9BKrF72/giphy.gif)

##### Learning Objectives

- Start to identify and implement use of Dev Tools and React Dev Tools.

---

##### Prerequisites

- JavaScript
- React
- React DevTools Chrome Extension

---

## Getting Started

1. If you haven't already, take a look through the lecture to familiarize yourself with DevTools as a concept, Chrome DevTools and React DevTools.

---

## Messing with DevTools

### What Are DevTools?

Browser Developer Tools, or DevTools, allow developers to collect information about web applications. DevTools are available for all browsers, but for this lesson, we will be talking about Chrome DevTools.

For mac users, open up a new window in chrome, and open your inspector tab by right clicking `cmd + click` anywhere on the document. Select `Inspect`.

Notice the tabs that are included in the DevTools, Elements, Console, Network, Sources, Performance, Memory, Application, and Security. See the table below for general functionality & additional reading.

|      Name       |                                      Purpose                                       |         Link         |
| :-------------: | :--------------------------------------------------------------------------------: | :------------------: |
|  **Elements**   |                   Inspect, select and modify elements on the DOM                   | https://rb.gy/4w1lqz |
|   **Console**   |       View logged message, use REPL in browser & other utility functionality       | https://rb.gy/buq76z |
|   **Network**   |   Generally checks that resources are being downloaded and uploaded as expected    | https://rb.gy/kf1l4x |
|   **Sources**   |       View files, edit CSS and JS, create and save snippets of JS & debug JS       | https://rb.gy/lkwqf0 |
| **Performance** |                            Analyze Runtime Performance                             | https://rb.gy/cobshn |
|   **Memory**    |                                Check Memory Storage                                | https://rb.gy/zrfopw |
| **Application** | Inspect local and session storage, cookies, cache, images, fonts, and stylesheets. | https://rb.gy/u17nck |
|  **Security**   |                           Inspects security of the page                            | https://rb.gy/wfs4gv |

---

#### The Element Panel

![Credit: Chrome DevTools Docs](https://developers.google.com/web/tools/chrome-devtools/images/panels/elements.png)

The Element Panel is typically the default panel that is opened up in the inspector. This panel shows you the DOM Tree, or the document object model. This shows what your HTML looks like on render, and shows how the CSS you wrote is applied to each element.

This panel also allows you to select and edit HTML elements and CSS properties.

---

##### Viewing & Changing the DOM

To select an HTML element, click on the element you want by finding it in the document object model, or use the built-in selector ![](https://developers.google.com/web/tools/chrome-devtools/css/imgs/select-an-element.png) to get that element.

To edit elements, right click (or double click) on the attribute (think class and id) or text directly. You can also right click on the element and you'll see a menu pop up menu with options to edit an element as HTML, delete an element, copy the outerHTML, or even copy the JSPath for a selected element.

---

##### Getting To Know CSS: Solving for Layout Issues

![Credit: Chrome DevTools Docs](https://developers.google.com/web/tools/chrome-devtools/css/imgs/aloha.png)
<br />
Within the element panel, you can also view and edit CSS that has been applied to elements on the page. Listed under "Styles", this section is scrollable and has a few key features, you can:

- View applied and inherited styles
- Remove styles by toggling the state of the checkboxes
- Access styles by the line number where the style rule has been applied
- Edit applied and inherited styles
- Filter Styles
- The Box Model
- Accessing and Toggling Psuedo-classes

**Notes**:

- Applied styles are styles that the user applies to an element, while inherited styles are inherited by elements from their parents.
  More on that here: https://rb.gy/3lopor
- Psuedo-classes in CSS: https://rb.gy/zl77vm

**_The Warning Section:_**

While Styles and Computed sections are great resources, note the following:

- If a user edits inherited or applied styles directly in the Styles tab, these will not be automatically applied to you code. The user will have to transfer these styles to their local files and save them there. On refresh, all changed will be lost, so users should be careful to transfer styles as they update.
- The Computed tab does not exist on the wide DevTools window, and is shown directly in the Styles tab.

---

#### Debugging & JavaScript

![](https://i.redd.it/m0xy5opltgm11.jpg)

Debugging code is a part of your new life as a programmer, and it can distinguish and more junior developer from a more skilled developer. When starting out debugging, a good deal of developers use `console.log` to manually log the outputs of functions they are inspecting to the console. While this method certainly works, it's not really the most efficient way to go about debugging, and unless you're careful in your code cleanup, you could end up with random information continously logging to your console.

<br/>

![](https://media.giphy.com/media/oOikYAQn9xfEEUXIyk/giphy.gif)

Cue Chrome DevTools.

Navigate over to the **Sources** tab in your inspect and click on it. You'll see a tab that looks something like this: <br/>![Credit: Chrome DevTools](https://developers.google.com/web/tools/chrome-devtools/javascript/imgs/sources-annotated.png)

The **Sources** tab has three parts, the File Navigation on the left, the Code Editor on the right, and the JS Debugging Pane on the bottom.

The way we test our code using the Chrome Debugger is by setting **breakpoints** within our code. A **breakpoint** is a point in our code where we want to pause execution, so we can inspect the outputs & identify problems in our code. This is especially valuable because unlike using `console.log`, a using a breakpoint in the Debugger can actually show all of the variables defined in both local and global scope at the time the function is called (and there are additional control measures, such as global and event listener breakpoints).

Well, how do we add a breakpoint to our code? In the **Sources** tab, select a file, and then the point where you want the breakpoint to be set on the opening line of a function.

The code then executes to that breakpoint, where the code pauses. The browser then presents an overlay that has two buttons. The first button is for resuming the script execution—which will continue to the run the script until the next breakpoint or its' natural end—while the second button is for **_Stepping Over_** the next function call, which will execute the function without stepping into it.

For more on this, see the **_Extra Reading & Resources_** section below.

---

### React DevTools

![Credit: React DevTools](https://lh3.googleusercontent.com/W5h-3Esx-a2cOq4TaQ2O5tz-zLMjTupUgJjiFF_wZfszDGHdlGpH0JeZoT29399vLdkRRQqBEeM=w640-h400-e365)

React DevTools is an extension that provide users with the ability to inspect component hierarchies; search through components; identify props, state, and hooks; and even allows the ability to record performance (how many times a component renders, and at what speed) of your app.

---

#### Components

The components tab shows a hierarchy of all rendered components (demonstrating the flow of component relationships), as well as a search area that demonstrates props & state (among other React features).

Within the components tab, a user can also access components in the console by selecting the bug icon in the top left corner. To select a component and open it up in the console, first select it, then click the bug icon. The component will log to the console containing all relevant information.

The profiler tab in React DevTools also allows a user to track and record information about how quickly your app renders. The profiler tab will give a visual output for each re-render, and makes tracking site performance in react extremely powerful.

> **_Question_**: Why might we use the Profiler tab?

For more on that, see the **_Extra Reading & Resources_** section below.

---

### You Do: Explore DevTools

Take a look at the React ATM Lab repo used in yesterday's lesson. Inspect it with React DevTools.

- Change an element
- Change an attribute
- Change some inherited styles
- Inspect the React Component tree
- Inspect props and state

---

### Takeaways

- How do we view and edit the DOM in the browser?
- How do we use the box model in DevTools to better understand our elements?
- How do we search for, or filter, style properties in the elements pane?
- How do we see all styles an element contains?
- What is the purpose of the Chrome Debugger? How can we use it to better our understanding of how code executes?
- What is the purpose of React DevTools? What are some ways this could come in handy?

---

### Extra Reading & Resources

- [React DevTools Tutorial](https://react-devtools-tutorial.now.sh/)
- [Getting Started with Debugging in Chrome DevTools](https://developers.google.com/web/tools/chrome-devtools/javascript)
- [The Network Tab](https://developers.google.com/web/tools/chrome-devtools/network)
- [Chrome DevTools Keyboard Shortcuts](https://developers.google.com/web/tools/chrome-devtools/shortcuts)
- [Accessiblity in Chrome DevTools](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference)
- [Storage in Chrome DevTools: Cookies, LocalStorage, and Cache](https://developers.google.com/web/tools/chrome-devtools/storage/cookies)
- [The React Profiler](https://reactjs.org/blog/2018/09/10/introducing-the-react-profiler.html)
