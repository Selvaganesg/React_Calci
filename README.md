# Ex04 Simple Calculator - React Project
## Date:

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

```
app.jsx

import React, { useState } from "react";
import "./Calculator.css"; 

function Calculator() {
  const [input, setInput] = useState("");

  const handleClick = (value) => {
    setInput(input + value);
  };

  const handleClear = () => {
    setInput("");
  };

  const handleCalculate = () => {
    try {
      setInput(eval(input).toString());
    } catch {
      setInput("Error");
    }
  };

  return (
    <div className="app-container">
      <div className="calculator">
        <h2>React Calculator</h2>
        <div className="display">{input || "0"}</div>
        <div className="buttons">
          <button onClick={handleClear}>C</button>
          <button onClick={() => handleClick("/")}>/</button>
          <button onClick={() => handleClick("*")}>*</button>
          <button onClick={() => handleClick("-")}>-</button>
          <button onClick={() => handleClick("7")}>7</button>
          <button onClick={() => handleClick("8")}>8</button>
          <button onClick={() => handleClick("9")}>9</button>
          <button onClick={() => handleClick("+")}>+</button>
          <button onClick={() => handleClick("4")}>4</button>
          <button onClick={() => handleClick("5")}>5</button>
          <button onClick={() => handleClick("6")}>6</button>
          <button onClick={() => handleClick("1")}>1</button>
          <button onClick={() => handleClick("2")}>2</button>
          <button onClick={() => handleClick("3")}>3</button>
          <button onClick={() => handleClick("0")}>0</button>
          <button onClick={handleCalculate}>=</button>
        </div>
      </div>
    </div>
  );
}

export default Calculator;

app.css

.calculator {
  width: 250px;
  margin: 50px auto;
  padding: 20px;
  border-radius: 12px;
  background: #222;
  color: white;
  text-align: center;
}

.display {
  background: #333;
  padding: 15px;
  border-radius: 8px;
  margin-bottom: 15px;
  font-size: 1.5rem;
  text-align: right;
}

.buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 10px;
}

button {
  padding: 15px;
  border: none;
  border-radius: 8px;
  background: #444;
  color: white;
  font-size: 1rem;
  cursor: pointer;
  transition: 0.2s;
}/* Center the calculator in the middle of the page */
.app-container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh; /* full viewport height */
  background: linear-gradient(135deg, #6a11cb, #2575fc);
}

/* Calculator box */
.calculator {
  background-color: white;
  padding: 25px;
  border-radius: 15px;
  box-shadow: 0px 8px 20px rgba(0, 0, 0, 0.2);
  width: 300px;
  text-align: center;
}

/* Display section */
.display {
  background-color: #222;
  color: white;
  font-size: 2rem;
  padding: 10px;
  border-radius: 10px;
  margin-bottom: 15px;
  overflow-x: auto;
}

/* Button grid layout */
.buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 10px;
}

/* Buttons styling */
button {
  padding: 15px;
  font-size: 1.2rem;
  border: none;
  border-radius: 10px;
  background-color: #2575fc;
  color: white;
  cursor: pointer;
  transition: 0.3s;
}

button:hover {
  background-color: #1a5ed8;
}

button:active {
  transform: scale(0.95);
}

/* Header text */
h2 {
  color: #333;
  margin-bottom: 15px;
}


button:hover {
  background: #666;
}

.equal {
  background: #4caf50;
}


```

## OUTPUT
![alt text](<Screenshot 2025-10-15 084416.png>)

## RESULT
The program for developing a simple calculator in React.js is executed successfully.
