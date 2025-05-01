# MWAD-EXP_04-Simple-caluculator
## Date:
### Name : Vikram K
### Reg No : 212222040180
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

### calculator.jsx
```
import React, { useState } from "react";

const Calculator = () => {
  const [input, setInput] = useState("");

  const handleClick = (value) => {
    setInput((prevInput) => prevInput + value);
  };

  const clearInput = () => {
    setInput("");
  };

  const calculateResult = () => {
    try {
      setInput(eval(input).toString());
    } catch (error) {
      setInput("Error");
    }
  };

  return (
    <div className="calculator">
      <h2>Calculator</h2>
      <input type="text" value={input} readOnly className="display" />
      <div className="button-grid">
        <button onClick={clearInput} className="operator">
          C
        </button>
        <button onClick={() => handleClick("/")} className="operator">
          /
        </button>
        <button onClick={() => handleClick("*")} className="operator">
          *
        </button>
        <button onClick={() => handleClick("-")} className="operator">
          -
        </button>

        <button onClick={() => handleClick("7")}>7</button>
        <button onClick={() => handleClick("8")}>8</button>
        <button onClick={() => handleClick("9")}>9</button>
        <button onClick={() => handleClick("+")} className="operator">
          +
        </button>

        <button onClick={() => handleClick("4")}>4</button>
        <button onClick={() => handleClick("5")}>5</button>
        <button onClick={() => handleClick("6")}>6</button>
        <button onClick={() => handleClick(".")} className="dot">
          .
        </button>

        <button onClick={() => handleClick("1")}>1</button>
        <button onClick={() => handleClick("2")}>2</button>
        <button onClick={() => handleClick("3")}>3</button>
        <button onClick={() => handleClick("0")}>0</button>
        <button onClick={calculateResult} className="equal">
          Click To Get Answer
        </button>
      </div>
      <h4>Name : Vikram K</h4>
      <h3>Reg No : 212222040180 </h3>
    </div>
  );
};

export default Calculator;
```
### index.css
```
body {
  margin: 0;
  padding: 0;
  background-color: #f2f2f2;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}

.app {
  text-align: center;
}

h2 {
  margin-bottom: 20px;
}

.calculator {
  background-color: #ffffff;
  padding: 30px;
  border-radius: 12px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  width: 320px;
}

.display {
  width: 90%;
  height: 50px;
  font-size: 24px;
  text-align: right;
  padding: 10px;
  margin-bottom: 20px;
  border: 1px solid #ccc;
  border-radius: 8px;
}

.button-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 10px;
}

button {
  height: 50px;
  font-size: 18px;
  border: none;
  border-radius: 8px;
  background-color: #e0e0e0;
  cursor: pointer;
  transition: background-color 0.2s ease;
}

button:hover {
  background-color: #d0d0d0;
}

.operator {
  background-color: #f9a825;
  color: white;
}

.operator:hover {
  background-color: #f57f17;
}

.equal {
  grid-column: span 1;
  background-color: #4caf50;
  color: white;
  width:440%;
}

.equal:hover {
  background-color: #388e3c;
}

.dot {
  grid-column: span 1;
}
```
## OUTPUT
![image](https://github.com/user-attachments/assets/d90b0d8f-73c1-4dea-8c11-0736462d1f48)


## RESULT
The program for developing a simple calculator in React.js is executed successfully.
