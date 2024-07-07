## Objective:
Design a Webpage using JavaScript eith a minimum of five mathematical operations.
## Description:
This Standard Calculator Has Been Created By Using Javascript And With the Help Of HTML And CSS
This Standard Calculator Has Different Mathematical Operators
## Code:
App.js
```c
let screen = document.getElementById('screen');
buttons = document.querySelectorAll('button');
let screenValue = '';
for (item of buttons) {
    item.addEventListener('click', (e) => {
        buttonText = e.target.innerText;
        console.log('Button text is ', buttonText);
        if (buttonText == 'X') {
            buttonText = '*';
            screenValue += buttonText;
            screen.value = screenValue;
        }
        else if (buttonText == 'C') {
            screenValue = "";
            screen.value = screenValue;
        }
        else if (buttonText == '=') {
            screen.value = eval(screenValue);
        }
        else {
            screenValue += buttonText;
            screen.value = screenValue;
        }
    })
}
```
Page.html
```c

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Calculator</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="container">
        <h1><U>CALCULATOR</U></h1>
        <h3 class="text"><U><I>RAHUL K(212221043006)</I></U></h3><br>

        <div class="calculator">
            <input type="text" name="screen" id="screen">
            <table>
                <tr>
                    <td><button class="color">(</button></td>
                    <td><button class="color">)</button></td>
                    <td><button class="color">C</button></td>
                    <td><button class="color">%</button></td>
                </tr>
                <tr>
                    <td><button>7</button></td>
                    <td><button>8</button></td>
                    <td><button>9</button></td>
                    <td><button class="color">*</button></td>
                </tr>
                <tr>
                    <td><button>4</button></td>
                    <td><button>5</button></td>
                    <td><button>6</button></td>
                    <td><button class="color">-</button></td>
                </tr>
                <tr>
                    <td><button>1</button></td>
                    <td><button>2</button></td>
                    <td><button>3</button></td>
                    <td><button class="color">+</button></td>
                </tr>
                <tr>
                    <td><button>0</button></td>
                    <td><button class="color">.</button></td>
                    <td><button class="color">/</button></td>
                    <td><button class="color">=</button></td>
                </tr>
            </table>
        </div>
    </div>

    <script src="app.js"></script>
</body>
</html>
```
Style.css
```c
.container {
    background-color: black;
    text-align: center;
    margin-top: 23px;
}

.calculator {
    border: none;
    background-color: #868686;
    padding: 30px;
    border-radius: 0px;
    display: inline-block;
}

h1 {
    font-size: 40px;
    font-family: Arial, Helvetica, sans-serif;
    color: white;
}

h3 {
    font-size: 20px;
    font-weight: bold;
    color: rgb(255, 253, 253);
    text-align: center;
    margin: auto;
    margin-top: 20px;
}

input {
    text-align: right;
    border-radius: 21px;
    border: 2px solid rgb(255, 174, 0);
    padding: 20px;
    background: rgb(242, 241, 241);
    font-size: 40px;
    height: 60px;
    width: 290px;
    color: rgb(11, 11, 11);
}

table {
    margin: auto;
}

button {
    border-radius: 20px;
    border: 0;
    outline: 0px;
    box-shadow: -8px -8px 15px rgba(180, 180, 180, 0.1),  5px 5px 15px rgba(0, 0, 0, 0.2);
    font-size: 20px;
    background: rgb(209, 157, 12);
    color: rgb(11, 11, 11);
    width: 60px;
    height: 60px;
    margin: 6px;
    cursor: pointer;
}

.color {
    color: rgb(255, 58, 58);
}
```
## Output:
![alt text](<Screenshot (56).png>)
![alt text](<Screenshot (57).png>)