# Temperature Conversion

## Description
A simple web application that converts temperatures between Celsius and Fahrenheit. Users can input a temperature, select the desired conversion, and see the result.

## Features
- Convert temperatures from Celsius to Fahrenheit and vice versa.
- Displays the converted temperature with one decimal place.
- Simple and intuitive user interface.

## Technologies Used
- HTML
- CSS
- JavaScript

## Usage
1. Open `index.html` in your web browser.
2. Enter a temperature value in the input box.
3. Select the desired conversion (Celsius to Fahrenheit or Fahrenheit to Celsius).
4. Click the "Submit" button to see the converted temperature.

## How to Run
1. Clone the repository or download the project files.
2. Open `index.html` in any web browser.
3. Enter a temperature value, select a conversion, and click "Submit" to see the result.

## JavaScript Explanation
The `weather.js` file contains the following:

### Variables
- **textBox**: References the input element where the user enters the temperature.
- **toFahrenheit**: References the radio button for converting Celsius to Fahrenheit.
- **toCelsius**: References the radio button for converting Fahrenheit to Celsius.
- **result**: References the paragraph element where the result will be displayed.

### Function: convert
- **Purpose**: Converts the entered temperature based on the selected conversion unit.
- **Functionality**:
  - Gets the value from the input box and converts it to a number.
  - Checks which radio button is selected (Celsius to Fahrenheit or Fahrenheit to Celsius).
  - Performs the appropriate conversion calculation.
  - Updates the text content of the result element with the converted temperature.

```javascript
// get references to the elements
const textBox = document.getElementById("textBox");
const toFahrenheit = document.getElementById("toFahrenheit");
const toCelsius = document.getElementById("toCelsius");
const result = document.getElementById("result");

// function to convert temperatures
function convert() {
    let temp = Number(textBox.value);

    if (toFahrenheit.checked) {
        temp = temp * 9 / 5 + 32;
        result.textContent = temp.toFixed(1) + "°F";
    } else if (toCelsius.checked) {
        temp = (temp - 32) * 5 / 9;
        result.textContent = temp.toFixed(1) + "°C";
    } else {
        result.textContent = "Select a unit";
    }
}
```

<br>

![tempimage](https://github.com/user-attachments/assets/96313c31-b59c-4104-90a2-acb0a1de0add)

