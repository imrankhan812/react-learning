## useState Hook (Memory)
* `useState` React ki temporary memory hai.
* Jab variable badalta hai, to yeh screen ko automatic refresh (re-render) kar deta hai.

## Conditional Rendering (Limit Control)
* `if (count < 4)` lagane se hum state ko ek limit par freeze kar sakte hain.
* Yeh real-world mein OTP limits ya shopping cart max quantity selector mein use hota hai.
* ## 3. Arrow Function and Brackets Rule `{ }`

React mein button ke click event (`onClick`) par brackets kab lagane hain aur kab nahi, iska simple rule yeh hai:

### 1. Jab sirf EK state change karni ho (Single Line):
Agar sirf ek kaam karna ho to curly braces `{ }` ki zaroorat nahi hoti. Arrow `=>` ke baad direct code likh dete hain.
* **Example:** `onClick={() => setCounter(count + 1)}`

### 2. Jab EK SE ZYADA (Multiple) states change karni hon (Block of Code):
Jab 2 ya us se zyada states ko ek sath update karna ho, to arrow `=>` ke baad **curly braces `{ }`** lagana LAZMI hai. Is boundary ke andar har statement ke aakhir mein semicolon `;` bhi lagaya jata hai.
* **Example:**
  ```jsx
  onClick={() => {
      setCounter(5);     // Kaam #1
      setIncrease(10);   // Kaam #2
  }}
