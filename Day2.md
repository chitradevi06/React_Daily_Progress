📌 Day 2 – JavaScript: Asynchronous Operations & Spread/Rest
🔹 Part 1: Asynchronous Operations
Why Asynchronous?

JS is single-threaded → async lets tasks run without blocking.

Browser/Node.js manages tasks → notifies JS when done.

1. Callbacks (Old Way)

Function executed later.

Example:

setTimeout(() => console.log("Later"), 2000);


Problem → Callback Hell (nested, hard to manage).

2. Promises (Better Way)

Represents eventual completion (success/failure).

States: Pending → Fulfilled → Rejected.

Methods: .then(), .catch().

Example:

fetchData()
  .then(data => processData(data))
  .catch(err => console.error(err));


Advantage → chaining & cleaner error handling.

3. Async / Await (Modern Way)

Syntactic sugar over Promises.

Looks synchronous but non-blocking.

Example:

async function handleData() {
  try {
    let data = await fetchData();
    let result = await processData(data);
    console.log(result);
  } catch (err) {
    console.error(err);
  }
}


Advantage → readable & easy error handling with try/catch.

✅ Common in React for API fetching.

🔹 Part 2: Spread & Rest (...)
1. Spread Operator → Spreading things out

Arrays: copy, merge, pass as args.

const arr = [1,2,3];
const copy = [...arr];  
const merged = [...arr, 4, 5];  
sum(...arr);  


Objects: copy, merge (later overwrites).

const user = {name:"Alice"};  
const newUser = {...user, age:25};  


✅ Common in React (props, state updates).

2. Rest Operator → Gathering things together

Collects remaining items into an array/object.

Example:

function logMessages(source, ...msgs) {
  console.log(source, msgs);
}
logMessages("System", "Start", "Ready");  
// msgs = ["Start","Ready"]


Used in function params & destructuring.

🔑 Interview Takeaways

Async evolution → Callbacks → Promises → Async/Await.

Spread → expands (copy, merge, pass args).

Rest → collects (function params, destructuring).

Mastering both is crucial in React & modern JS.
