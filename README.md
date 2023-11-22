# calculator
<!DOCTYPE html>
<html>
<head>
    <title>SIMPLE CALCULATOR</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color:purple;
            margin: 0;
            font-family: 'Arial';
            font-weight: 800;
        }
        #calculator {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            max-width: 400px;
            gap: 10px; 
        }
        #display {
            grid-column: span 4;
            height: 50px;
            background-color:white;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 0 10px;
             font-size: 24px;
        }
        button {
            height: 50px;
            font-size: 24px;
        }
        p{
            color:white;
            text-align: center;
            font-family:'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
            
        }
    </style>
</head>

<body>
    <div id="calculator">
        <p>CALCULATOR</p>
        <div id="display"></div>
        
        <button class="numButton" onclick="display('1')">1</button>
        <button class="numButton" onclick="display('2')">2</button>
        <button class="numButton" onclick="display('3')">3</button>
        <button class="opButton" onclick="display('+')">+</button>
        <button class="numButton" onclick="display('4')">4</button>
        <button class="numButton" onclick="display('5')">5</button>
        <button class="numButton" onclick="display('6')">6</button>
        <button class="opButton" onclick="display('-')">-</button>
        <button class="numButton" onclick="display('7')">7</button>
        <button class="numButton" onclick="display('8')">8</button>
        <button class="numButton" onclick="display('9')">9</button>
        <button class="opButton" onclick="display('*')">*</button>
        <button class="numButton" onclick="display('0')">0</button>
        <button class="opButton" onclick="display('/')">/</button>
        <button class="eqButton" onclick="calculate()">=</button>
        <button class="clearButton" onclick="myfunction()">c</button>
    </div>

    <script>

        function add(a, b) {
            return a + b;
        }

        function subtract(a, b) {
            return a - b;
        }

        function multiply(a, b) {
            return a * b;
        }

        function divide(a, b) {
            if (b == 0) {
                return "Error! Division by zero is undefined";
            } else {
                return a / b;
            }
        }

        function display(value) {
            var result = document.getElementById("display");
            result.textContent += value;
        }

       
        function calculate() {
            var result = document.getElementById("display");
            var resultValue = eval(result.textContent);
            result.textContent = resultValue;
        }
        function myfunction() {
            var result = document.getElementById("display");
			var resultValue = eval(result.textContent);
            result.textContent = "";
        }

    </script>
</body>

</html>
