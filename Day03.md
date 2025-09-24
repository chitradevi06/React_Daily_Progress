📌 Day 3 – JavaScript Destructuring

🔹 Why Destructuring?
Cleaner code → shorter, easier to read.
Efficient access → quickly extract needed values.
Works with objects ({}) and arrays ([]).

1. Object Destructuring ({})

Extract properties into variables using curly braces.

const person = {
firstName: "Alice",
age: 30,
city: "Wonderland" };

const { firstName, age } = person;
console.log(firstName, age); // Alice 30


✅ Bonus Features

Renaming variables:

const { firstName: fName, age: personAge } = person;
console.log(fName, personAge); // Alice 30


Default values:

const { country = "Unknown" } = person;
console.log(country); // Unknown

2. Array Destructuring ([])

Extract elements by position (index).

const colors = ["red", "green", "blue"];
const [firstColor, secondColor] = colors;
console.log(firstColor, secondColor); // red green


✅ Bonus Features

Skipping elements:

const numbers = [10, 20, 30];
const [first, , third] = numbers;
console.log(first, third); // 10 30


Rest syntax:

const scores = [100, 95, 88];
const [top, ...others] = scores;
console.log(top, others); // 100 [95, 88]



Default values:

const settings = ["dark"];
const [theme = "light", fontSize = 16] = settings;
console.log(theme, fontSize); // dark 16

🔑 Interview Takeaways
Object destructuring → pick properties by name.
Array destructuring → pick values by position.

Supports renaming, skipping, rest syntax, and defaults.

Very common in React props & state management.
