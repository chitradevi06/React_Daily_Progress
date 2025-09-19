# Day 1 - Learning Notes

## 🌟 ES6 (ECMAScript 2015)
- ES6 introduced many new features in JavaScript to make code more readable and powerful.
- Some key features:
  - `let` and `const` for variable declarations.
  - Arrow functions `()=>`.
  - Template literals using backticks `` ` ``.
  - Default parameters.
  - Destructuring.

---

## 🔹 Variables in ES6
- **`var`**: Function scoped or globally scoped. Can be redeclared & updated.  
- **`let`**: Block scoped. Can be updated but **not redeclared** in the same scope.  
- **`const`**: Block scoped. **Cannot be updated or redeclared**.  

### Example:
```javascript
var a = 10;  // function/global scope
let b = 20;  // block scope
const c = 30; // block scope, cannot change

b = 25;      // ✅ allowed
// c = 35;   // ❌ Error: Assignment to constant variable
