<h1>Modern Calculator</h1> 
<h4>Youtube Tutorial Link : </h4>

<b> Features: </b> 
- Summation 
- Substraction
- Multiplication
- Divition 

<b> Built With: </b> 
- HTML5
- CSS
- JavaScript
- Document Object Model

<b>Preview:</b> 
![](/images/desktop-view.JPG)


<b>Codes I am Proud Of:</b> 

```js
function clearDisplay() {
    document.getElementsByName("display")[0].value = "";
}

function deleteLastChar() {
    var display = document.getElementsByName("display")[0];
    display.value = display.value.toString().slice(0, -1);
}

function addDecimal() {
    document.getElementsByName("display")[0].value += ".";
}

function addOperator(operator) {
    document.getElementsByName("display")[0].value += operator;
}

function addNumber(number) {
    document.getElementsByName("display")[0].value += number;
}

function calculate() {
    var displayValue = document.getElementsByName("display")[0].value;
    
    var result;

    // Split the display value by the operator
    var parts = displayValue.split(/(\+|-|\*|\/)/);

    // Check if there are exactly three parts (number, operator, number)
    if (parts.length === 3) {
        // Get the first number, the operator and the second number
        var num1 = Number(parts[0]);
        var op = parts[1];
        var num2 = Number(parts[2]);

        // Perform the calculation based on the operator
        if (op === "+") {
            result = num1 + num2;
        } else if (op === "-") {
            result = num1 - num2;
        } else if (op === "*") {
            result = num1 * num2;
        } else if (op === "/") {
            // Check for division by zero
            if (num2 !== 0) {
                result = num1 / num2;
            } else {
                result = "Error";
            }
        } else {
            // Invalid operator
            result = "Error";
        }
    } else {
        // Invalid expression
        result = "Error";
    }

    document.getElementsByName("display")[0].value = result;
    Copy
}
```

