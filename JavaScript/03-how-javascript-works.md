# 02. How JavaScript Works?

**Difficulty:** 🟢 Easy

## Question

How does JavaScript work internally?

---

## Answer

When JavaScript code runs:

1. The JavaScript engine parses the code.
2. The engine compiles it using JIT (Just-In-Time) compilation.
3. An execution context is created.
4. The call stack manages function execution.
5. The event loop handles asynchronous tasks.

---

## Flow

```text
[ JavaScript Source Code ]
           │
           ▼
     ┌───────────┐
     │  Parser   │  ──> (Tokenizes code into an Abstract Syntax Tree / AST)
     └───────────┘
           │
           ▼
   ┌───────────────┐
   │  Interpreter  │  ──> (Quickly generates and starts executing Bytecode)
   └───────────────┘
     │           ▲
     │ (Profile) │ (Optimize hot code blocks)
     ▼           │
   ┌───────────────┐
   │ JIT Compiler  │  ──> (Produces highly optimized Machine Code)
   └───────────────┘
           │
           ▼
┌─────────────────────┐
│  Execution Phase    │  ──> (Managed via Call Stack & Memory Heap)
└─────────────────────┘


## Quick Example: Visualizing the Execution

console.log("Start");

setTimeout(() => {
console.log("Timeout Callback");
}, 0);

Promise.resolve().then(() => {
console.log("Promise Callback");
});

console.log("End");

## Execution Step-by-Step Chronology:

1. console.log("Start") enters the Call Stack, prints Start, and pops off.

2. setTimeout enters the Call Stack. The runtime registers the timer web API, handles the 0ms delay instantly, and passes the anonymous arrow function to the Callback Queue. setTimeout pops off the stack.

3. Promise.resolve().then(...) enters the Call Stack. The success callback is immediately queued into the Microtask Queue. The Promise logic pops off the stack.

4. console.log("End") enters the Call Stack, prints End, and pops off. The script execution finishes; the Call Stack is now entirely empty.

5. The Event Loop activates. It checks the high-priority Microtask Queue first, finds the Promise callback, pushes it onto the Call Stack, logs Promise Callback, and pops it off.

6. The Microtask queue is empty. The Event Loop checks the Callback Queue, finds the setTimeout callback, pushes it onto the Call Stack, logs Timeout Callback, and pops it off.

## Interview Follow-up Questions

- What is parsing?
- What is JIT Compilation?
- What is an Execution Context?
