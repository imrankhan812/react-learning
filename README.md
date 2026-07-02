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
## 4. Toggle Concept & Real-World Uses
Toggle ka matlab hai ek hi state ko ON/OFF ya True/False mein switch karna.
* **Mobile Navbar:** Button click par menu ka show aur hide hona.
* **Dark Mode:** Light aur dark theme ke darmiyan switch karna.
* **FAQs Section:** Sawal par click karne se jawab ka open aur close hona.
* # React useState Concept

React mein `useState` tab use hota hai jab hum chahte hain ke variable ki value badalne par **screen bhi automatic update (render) ho**.

## Syntax:
```jsx
const [count, setCount] = useState(0);
