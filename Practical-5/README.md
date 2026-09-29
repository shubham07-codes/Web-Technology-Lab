# Practicle No. 5

## Aim

To create an interactive calculator using JavaScript events and event handling.

## Problem Definition

Build an interactive Calculator that responds to button clicks and key presses and updates the result dynamically.

## Theory

JavaScript events are actions performed by the user, such as clicking a button or pressing a keyboard key. Event handling allows JavaScript to respond to these actions. In this practical, a calculator is created using HTML and JavaScript. Click and keyboard events are used to enter numbers, perform calculations, clear the display, and show results dynamically.

## Procedure and Execution

### Steps for Implementation

1. Create `index.html` and `script.js` files.
2. Create the calculator with number and operator buttons.
3. Create functions for calculation, clear, and delete.
4. Add click events to the calculator buttons.
5. Add keyboard events for user input.
6. Open the calculator in a browser and test it.

## HTML Code

```html
<!DOCTYPE html>
<html>
<head>
    <title>JavaScript Calculator</title>
</head>

<body>

    <h1>Simple Calculator</h1>

    <input type="text" id="display" readonly>

    <br><br>

    <button onclick="clearDisplay()">C</button>
    <button onclick="deleteLast()">DEL</button>
    <button onclick="addValue('/')">/</button>
    <button onclick="addValue('*')">*</button>

    <br><br>

    <button onclick="addValue('7')">7</button>
    <button onclick="addValue('8')">8</button>
    <button onclick="addValue('9')">9</button>
    <button onclick="addValue('-')">-</button>

    <br><br>

    <button onclick="addValue('4')">4</button>
    <button onclick="addValue('5')">5</button>
    <button onclick="addValue('6')">6</button>
    <button onclick="addValue('+')">+</button>

    <br><br>

    <button onclick="addValue('1')">1</button>
    <button onclick="addValue('2')">2</button>
    <button onclick="addValue('3')">3</button>
    <button onclick="calculate()">=</button>

    <br><br>

    <button onclick="addValue('0')">0</button>
    <button onclick="addValue('.')">.</button>

    <p id="message"></p>

    <script src="script.js"></script>

</body>
</html>
```

## JavaScript Code

```javascript
const display = document.getElementById("display");
const message = document.getElementById("message");

function addValue(value) {
    display.value = display.value + value;
}

function clearDisplay() {
    display.value = "";
    message.innerText = "";
}

function deleteLast() {
    display.value = display.value.slice(0, -1);
}

function calculate() {

    if (display.value === "") {
        message.innerText = "Please enter a calculation";
        return;
    }

    try {
        let result = eval(display.value);
        display.value = result;
        message.innerText = "Calculation Successful";
    }
    catch (error) {
        message.innerText = "Invalid Calculation";
    }
}

document.addEventListener("keydown", function(event) {

    const key = event.key;

    if (
        (key >= "0" && key <= "9") ||
        key === "+" ||
        key === "-" ||
        key === "*" ||
        key === "/" ||
        key === "."
    ) {
        addValue(key);
    }

    else if (key === "Enter") {
        calculate();
    }

    else if (key === "Backspace") {
        deleteLast();
    }

    else if (key === "Escape") {
        clearDisplay();
    }

});
```

## Output Analysis

The calculator accepts numbers and operators using button clicks or keyboard input. It calculates and displays the result dynamically. Clear, delete, Enter, Backspace, and Escape functions work correctly.

## Conclusion

In this practical, I learned how to use JavaScript click and keyboard events to create an interactive calculator and dynamically update the webpage.
