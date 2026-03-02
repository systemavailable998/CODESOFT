# CODESOFT (password generator)
<!DOCTYPE html>
<link rel="stylesheet" href="style.css" />
<link href="<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Password Generator | JavaScript Project</title>
    <link rel="stylesheet" href="style.css">
    <link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">
    <title>Password Generator | JavaScript Project</title>
</head>
<body>
<div class="container">
  <h1>Password Generator</h1>

  <div class="inputBox">
    <input type="text" class="passBox" id="passwordDisplay" readonly />
  </div>

  <div class="range">
    <input type="range" min="8" max="25" value="12" id="inputRange" />
    <p>Length: <span id="sliderValue">12</span></p>
  </div>
  <div class="row">
    <label for="lowercase">Include Lowercase Letters (a-z)</label>
    <input type="checkbox" name="lowercase" id="lowercase" />
  </div>

  <div class="row">
    <label for="uppercase">Include Uppercase Letters (A-Z)</label>
    <input type="checkbox" name="uppercase" id="uppercase" />
  </div>

  <div class="row">
    <label for="number">Include number (0-9)</label>
    <input type="checkbox" name="number" id="number" />
  </div>
  <div class="row">
    <label for="symbols">Include symbols (@-*)</label>
    <input type="checkbox" name="symbols" id="symbols" />
  </div>
  <button type="button" class="genBtn" id="genBtn">Generate Password</button>
</div>
<script src="script.js"></script>



#css password generator
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@500&display=swap');

*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Poppins', sans-serif;
}

body{
    width: 100%;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    background: linear-gradient(45deg, #0a0a0a, #3a4452);
}
.container {
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    background: linear-gradient(45deg, #0a0a0a, #3a4452);
}

.calculator {
    border: 1px solid #717377;
    padding: 20px;
    border-radius: 16px;
    background: transparent;
    box-shadow: 0px 3px 15px rgba(113, 115, 119, 0.5);
}
input {
    width: 320px;
    border: none;
    padding: 24px;
    margin: 10px;
    background: transparent;
    box-shadow: 0px 3px 15px rgba(84, 84, 84, 0.1);
    font-size: 40px;
    text-align: right;
    cursor: pointer;
    color: #ffffff;
}
button {
    border: none;
    width: 60px;
    height: 60px;
    margin: 10px;
    border-radius: 50%;
    background: transparent;
    color: #ffffff;
    font-size: 20px;
    box-shadow: -8px -8px 15px rgba(255, 255, 255, 0.1);
    cursor: pointer;
}

.equalBtn {
    background-color: #fb7c14;
}

#java script
let input = document.getElementById('inputBox');
let buttons = document.querySelectorAll('button');

let string = "";
let arr = Array.from(buttons);

arr.forEach(button => {
    button.addEventListener('click', (e) => {
        if (e.target.innerHTML == '=') {
            // Evaluates the string as a mathematical expression
            string = eval(string);
            input.value = string;
        } 
        else if (e.target.innerHTML == 'AC') {
            // Clears everything
            string = "";
            input.value = string;
        } 
        else if (e.target.innerHTML == 'DEL') {
            // Removes the last character
            string = string.substring(0, string.length - 1);
            input.value = string;
        } 
        else {
            // Appends the button value to the string
            string += e.target.innerHTML;
            input.value = string;
        }
    })
})
