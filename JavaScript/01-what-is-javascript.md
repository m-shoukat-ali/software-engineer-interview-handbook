# 01. What is JavaScript?

**Difficulty:** 🟢 Easy

## Question

What is JavaScript?

---

## Answer

JavaScript is a **high-level, interpreted, dynamically typed, and prototype-based programming language** primarily used to create interactive and dynamic web applications.

Initially, JavaScript was designed to run only in web browsers, but today it also runs on servers using **Node.js**, allowing developers to build full-stack applications using a single language.

JavaScript follows the **ECMAScript (ES)** standard, which defines its syntax and features.

---

## Key Characteristics

- High-level language
- Dynamically typed
- Interpreted (executed by a JavaScript engine like V8)
- Object-oriented (Prototype-based)
- Multi-paradigm
  - Procedural
  - Functional
  - Object-Oriented
- Single-threaded
- Asynchronous (using Event Loop)
- Cross-platform

---

## Example

```javascript
function greet(name) {
  return `Hello, ${name}!`;
}

console.log(greet("JavaScript"));
```

Output:

```
Hello, JavaScript!
```

---

## Where JavaScript is Used

- Web Applications
- Backend Development (Node.js)
- Mobile Apps (React Native)
- Desktop Apps (Electron)
- Browser Extensions
- Games
- Serverless Functions
- IoT Applications

---

## JavaScript Engine

Different browsers use different JavaScript engines.

| Browser | Engine         |
| ------- | -------------- |
| Chrome  | V8             |
| Edge    | V8             |
| Firefox | SpiderMonkey   |
| Safari  | JavaScriptCore |

Node.js also uses the **V8 Engine**.

---

## Advantages

- Easy to learn
- Huge ecosystem (npm)
- Fast execution
- Works on every modern browser
- Large community support
- Full-stack development with one language

---

## Limitations

- Single-threaded execution
- Dynamic typing may introduce runtime errors
- Browser compatibility issues for newer features (without transpilation)

---

## Real-World Use Cases

- Building Single Page Applications (React, Angular, Vue)
- REST APIs (Node.js + Express)
- Real-time chat applications
- Dashboards
- E-commerce websites

---

## Interview Follow-up Questions

1. Is JavaScript compiled or interpreted?
2. What is ECMAScript?
3. What is the V8 Engine?
4. Is JavaScript single-threaded?
5. How does JavaScript handle asynchronous operations?
6. What is the Event Loop?
7. What are JavaScript data types?
8. What is the difference between JavaScript and TypeScript?

---

## Common Mistakes

❌ JavaScript and Java are the same language.

No. They are completely different programming languages.

❌ JavaScript is only for frontend.

No. JavaScript can be used for backend development using Node.js.

❌ JavaScript is synchronous only.

No. JavaScript is single-threaded but supports asynchronous programming using callbacks, Promises, async/await, and the Event Loop.

---

## Quick Revision

- JavaScript is a high-level programming language.
- It follows the ECMAScript standard.
- Runs in browsers and on servers using Node.js.
- Uses the V8 engine in Chrome and Node.js.
- Single-threaded with asynchronous capabilities.
- Supports multiple programming paradigms.
