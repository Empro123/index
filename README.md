<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Simple Calculator</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background: #f4f4f4;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }

        .calculator {
            background: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }

        input {
            width: 100%;
            height: 50px;
            font-size: 20px;
            margin-bottom: 10px;
            text-align: right;
            padding-right: 10px;
        }

        button {
            width: 60px;
            height: 60px;
            font-size: 18px;
            margin: 5px;
            cursor: pointer;
        }
    </style>
</head>
<body>

<div class="calculator">
    <input type="text" id="result" disabled>

    <div>
        <button onclick="clearResult()">C</button>
        <button onclick="appendValue('/')">/</button>
        <button onclick="appendValue('*')">*</button>
        <button onclick="appendValue('-')">-</button>
    </div>

    <div>
        <button onclick="appendValue('7')">7</button>
        <button onclick="appendValue('8')">8</button>
        <button onclick="appendValue('9')">9</button>
        <button onclick="appendValue('+')">+</button>
    </div>

    <div>
        <button onclick="appendValue('4')">4</button>
        <button onclick="appendValue('5')">5</button>
        <button onclick="appendValue('6')">6</button>
        <button onclick="calculate()">=</button>
    </div>

    <div>
        <button onclick="appendValue('1')">1</button>
        <button onclick="appendValue('2')">2</button>
        <button onclick="appendValue('3')">3</button>
        <button onclick="appendValue('0')">0</button>
    </div>
</div>

<script>
    function appendValue(value) {
        document.getElementById("result").value += value;
    }

    function clearResult() {
        document.getElementById("result").value = "";
    }

    function calculate() {
        let expression = document.getElementById("result").value;
        document.getElementById("result").value = eval(expression);
    }
</script>

</body>
</html># index
