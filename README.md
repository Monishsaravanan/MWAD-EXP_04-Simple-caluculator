# MWAD-EXP_04-Simple-calculator

## Name: MONISH S

## Register Number: 212223040115

## AIM
To  develop a Simple Calculator using React.js with clean and responsive design, ensuring a smooth user experience across different screen sizes.

## ALGORITHM
### STEP 1
Create a React App.

### STEP 2
Open a terminal and run:
  <ul><li>npx create-react-app simple-calculator</li>
  <li>cd simple-calculator</li>
  <li>npm start</li></ul>

### STEP 3
Inside the src/ folder, create a new file Calculator.js and define the basic structure.

### STEP 4
Plan the UI: Display screen, number buttons (0-9), operators (+, -, *, /), clear (C), and equal (=).

### STEP 5
Create a new file Calculator.css in src/ and add the styling.

### STEP 6
Open src/App.js and modify it.

### STEP 7
Start the development server.
  npm start

### STEP 8
Open http://localhost:3000/ in the browser.

### STEP 9
Test the calculator by entering numbers and operations.

### STEP 10
Fix styling issues and refine content placement.

### STEP 11
Deploy the website.

### STEP 12
Upload to GitHub Pages for free hosting.

## PROGRAM
### App.jsx
```
import React from 'react'
import Calculator from './calculator'

const App = () => {
  return (
    <div className="App">
      <h1 style={{display:"flex",justifyContent:"center"}}>Simple React Calculator</h1>
      <Calculator/>
    </div>
  )
}

export default App

```

### Calculator.jsx
```
import React, { useState } from "react";
import "./Calculator.css";

const Calculator = () => {
  const [input, setInput] = useState("");
  const [result, setResult] = useState("");

  const handleClick = (value) => {
    setInput(input + value);
  };

  const handleClear = () => {
    setInput("");
    setResult("");
  };

  const handleEquals = () => {
    try {
      setResult(eval(input)); // simple evaluation
    } catch {
      setResult("Error");
    }
  };

  return (
    <div className="calculator">
      <div className="display">
        <div className="input">{input || "0"}</div>
        <div className="result">{result}</div>
      </div>
      <div className="buttons">
        {["7", "8", "9", "/"].map((btn) => (
          <button key={btn} onClick={() => handleClick(btn)}>
            {btn}
          </button>
        ))}
        {["4", "5", "6", "*"].map((btn) => (
          <button key={btn} onClick={() => handleClick(btn)}>
            {btn}
          </button>
        ))}
        {["1", "2", "3", "-"].map((btn) => (
          <button key={btn} onClick={() => handleClick(btn)}>
            {btn}
          </button>
        ))}
        {["0", ".", "C", "+"].map((btn) =>
          btn === "C" ? (
            <button key={btn} onClick={handleClear}>
              {btn}
            </button>
          ) : (
            <button key={btn} onClick={() => handleClick(btn)}>
              {btn}
            </button>
          )
        )}
        <button className="equals" onClick={handleEquals}>
          =
        </button>
      </div>
    </div>
  );
};

export default Calculator;

```

### Calculator.css
```
.calculator {
  width: 100%;
  max-width: 400px;
  margin: 50px auto;
  border-radius: 20px;
  overflow: hidden;
  background: linear-gradient(145deg, #ffffff, #e6e6e6);
  box-shadow: 8px 8px 15px #bebebe, -8px -8px 15px #ffffff;
  padding: 20px;
}

.display {
  background: #1e1e2f;
  color: #fff;
  padding: 20px;
  font-size: 2rem;
  text-align: right;
  border-radius: 15px;
  margin-bottom: 20px;
  box-shadow: inset 3px 3px 6px #14141f, inset -3px -3px 6px #2b2b42;
}

.input {
  font-size: 1.5rem;
  color: #f0f0f0;
}

.result {
  font-size: 1.2rem;
  color: #00ffcc;
}

.buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 15px;
}

button {
  padding: 20px;
  font-size: 1.5rem;
  border-radius: 15px;
  border: none;
  cursor: pointer;
  background: #f0f0f0;
  box-shadow: 5px 5px 10px #d1d1d1, -5px -5px 10px #ffffff;
  transition: all 0.2s;
}

button:hover {
  background: #e0e0e0;
  transform: translateY(-2px);
  box-shadow: 6px 6px 12px #c8c8c8, -6px -6px 12px #ffffff;
}

.equals {
  grid-column: span 4;
  background: #4caf50;
  color: white;
  box-shadow: 5px 5px 10px #3d8b3d, -5px -5px 10px #60d060;
}

.equals:hover {
  background: #45a049;
}

@media (max-width: 500px) {
  .calculator {
    padding: 15px;
  }

  button {
    padding: 15px;
    font-size: 1.2rem;
  }
}

```



## OUTPUT
<img width="1807" height="907" alt="image" src="https://github.com/user-attachments/assets/3384e5ee-3f14-4abf-b181-544858ceaf1b" />



## RESULT
The program for developing a simple calculator in React.js is executed successfully.
