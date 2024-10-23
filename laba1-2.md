![image](https://github.com/user-attachments/assets/fa281ad1-2f31-4acb-a5b1-a25551b520a9)

<!DOCTYPE html>
<html lang="ru">

<head>
    <meta charset="UTF-8">
    <title>Калькулятор</title>
    <link rel="stylesheet" href="style.css"> 
</head>

<body>
    <div class="background"></div>
    <div class="calculator">
        
    
        <div class="grid-container">
                <div id="result" class="result" style="padding-right: 15px">0</div>

                <button id="btn_op_clear" class="my-btn primary grid-item">C</button>
                <button id="btn_op_backspace" class="my-btn primary grid-item">-></button>
                <button id="btn_op_sign" class="my-btn primary grid-item">+/-</button>
                <button id="btn_op_div" class="my-btn primary grid-item">/</button>
                <button id="btn_op_percent" class="my-btn secondary grid-item">%</button>
                <button id="btn_op_k" class="my-btn k secondary grid-item">000</button>

                <button id="btn_digit_7" class="my-btn grid-item">7</button>
                <button id="btn_digit_8" class="my-btn grid-item">8</button>
                <button id="btn_digit_9" class="my-btn grid-item">9</button>
                <button id="btn_op_mult" class="my-btn primary grid-item">x</button>
                <button id="btn_op_sqrt" class="my-btn secondary grid-item">^1/2</button>

                <button id="btn_digit_4" class="my-btn grid-item">4</button>
                <button id="btn_digit_5" class="my-btn grid-item">5</button>
                <button id="btn_digit_6" class="my-btn grid-item">6</button>
                <button id="btn_op_minus" class="my-btn primary grid-item">-</button>
                <button id="btn_op_pow" class="my-btn secondary grid-item">^2</button>
                <button id="btn_op_resultcolorchange" class="my-btn resultcolorchange secondary grid-item">Смена цвета</button>     

                <button id="btn_digit_1" class="my-btn grid-item">1</button>
                <button id="btn_digit_2" class="my-btn grid-item">2</button>
                <button id="btn_digit_3" class="my-btn grid-item">3</button>
                <button id="btn_op_plus" class="my-btn primary grid-item">+</button>
                <button id="btn_op_factorial" class="my-btn secondary grid-item">!</button>
            
                <button id="btn_digit_0" class="my-btn grid-item">0</button>
                <button id="btn_digit_dot" class="my-btn grid-item">.</button>
                <button id="btn_op_equal" class="my-btn secondary execute grid-item">=</button>
        </div>
    </div>
    
    <div class="flex-container">
        <div class="flex-item">
        <div>
            <button id="theme" class="my-btn theme">Переключить тему</button>
            <script src="script.js"></script>
        </div>
    
        <div>ЛР выполнена Байназаровым Эриком Ильгизовичом</div>
    
        <div>
            <form>
                <label for="fruits">Выберите фрукт:</label>
                <select id="fruits" name="fruits">
                  <option value="orange">Яблоко</option>
                  <option value="banana">Банан</option>
                  <option value="apple">Апельсин</option>
                </select>
            </form>
        </div>
        </div>
        <div class="flex-item">
        
    
        <div>
            Цель данной лабораторной работы -
            <b>знакомство</b>
            с инструментами построения пользовательских интерфейсов web-сайтов: 
            <b>HTML, CSS</b>. В ходе выполнения работы, вам предстоит ознакомиться с
            кодом реализации простого калькулятора, и затем выполнить задания по варианту.</title>
        </div>
    
        <div> <a href="https://github.com/IgorSergeevichISIT/Web/blob/main/turorials/lab1/readme.md"> Нажми меня! </a> </div>

        <div>
            <details>
                <summary>Автор</summary>
                <p>Байназаров Эрик Ильгизович, ИС-22</p>
            </details>
        </div>

        </div>
    </div>
</body>
</html>



body {
    overflow: hidden;
    z-index: 1;
    width: 100vw;
    height: 100vh;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  }
  
  .background {
    background: #121212;
    width: 100%;
    height: 100%;
    position: absolute;
    z-index: -1;
    background: url("./photo/calc.jpg");
    background-size: cover;
    opacity: 0.3;
  }
  
  .flex-container {
    display: flex;
  }
  .flex-item {
    margin: 8px;
    text-align: left;
  }
  
  body.light-theme {
    background-color: #ffffff;
    color: #000000;
  }
  
  body.dark-theme {
    background-color: #121212;
    color: #ffffff;
  }
  
  .grid-container {
    display: inline-grid;
    grid-template-columns: repeat(6, 4em);
    grid-template-rows: repeat(7, 4em);
    gap: 10px;
  }
  
  .calculator{
    display: grid;
    place-items: center;
  }
  
  .my-btn { 
    font-weight: lighter;
    box-sizing: border-box;
    text-align: center;
    font-size: 1.8em;
    border-radius: 0%;
    border: none;
    background: rgb(117, 117, 117);
    color: #000000;
    cursor: pointer;             
    user-select: none;
  } 
  
  .my-btn:hover {
    background: rgb(211, 211, 211);
  }
  
  .my-btn:active {
    filter: brightness(130%);
  }
  
  .my-btn.theme {
    width: 220px;
    height: 50px;
    font-size: 1.3em;
    font-weight: lighter;
    filter: brightness(130%); 
  }
  
  .my-btn.primary { 
    background: #a0a0a0; 
  }
  
  .my-btn.secondary { 
    background: #656fca; 
  }
  
  .my-btn.execute {
    grid-column-start: 3;
    grid-column-end: 7;
    border-radius: 0px;
  }
  
  .my-btn.k {
    grid-column-start: 6;
    grid-column-end: 7;
    grid-row-start: 3;
    grid-row-end: 5;
    border-radius: 0px;
  }
  
  .my-btn.resultcolorchange {
    grid-column-start: 6;
    grid-column-end: 7;
    grid-row-start: 5;
    grid-row-end: 7;
    border-radius: 0px;
    font-size: 0.5em;
  }
  
  .result { 
    grid-column-start: 1;
    grid-column-end: 7;
    grid-row-start: 1;
    grid-row-end: 3;
    display: inline-block;
    background: gray;
    border-radius: 18px;             
    text-align: right;               
    color: white;
    font-size: 2em;
  }



  window.onload = function(){ 

    let a = ''
    let b = ''
    let expressionResult = ''
    let selectedOperation = null
  
    outputElement = document.getElementById("result")
    
    digitButtons = document.querySelectorAll('[id ^= "btn_digit_"]')
  
    function onDigitButtonClicked(digit) {
      if (!selectedOperation) {
          if (a === '' && digit === '0') return
          if ((digit != '.') || (digit == '.' && !a.includes(digit))) { 
              a += digit
          }
          outputElement.innerHTML = a
      } else {
        if (b === '' && digit === '0') return
          if ((digit != '.') || (digit == '.' && !b.includes(digit))) { 
              b += digit
              outputElement.innerHTML = b        
          }
      }
  }
  
  digitButtons.forEach(button => {
    button.onclick = function() {
        const digitValue = button.innerHTML
        onDigitButtonClicked(digitValue)
    }
  });
  
  document.getElementById("btn_op_mult").onclick = function() { 
    if (a === '') return
    selectedOperation = 'x'
  }
  document.getElementById("btn_op_plus").onclick = function() { 
    if (a === '') return
    selectedOperation = '+'
  }
  document.getElementById("btn_op_minus").onclick = function() { 
    if (a === '') return
    selectedOperation = '-'
  }
  document.getElementById("btn_op_div").onclick = function() { 
    if (a === '') return
    selectedOperation = '/'
  }
  
  document.getElementById("btn_op_backspace").onclick = function() {
    let updatedElement = outputElement.innerHTML
    updatedElement = updatedElement.substring(0, updatedElement.length - 1)
    outputElement.innerHTML = updatedElement
  
    if (!selectedOperation) {
      a = updatedElement
    } else {
      b = updatedElement
    }
  }
  
  document.getElementById("btn_op_sign").onclick = function() {
    if (!selectedOperation) {
      a = (+a) * -1
      outputElement.innerHTML = a
    } else {
      b = (+b) * -1
      outputElement.innerHTML = b
    }
  }
  
  document.getElementById("btn_op_percent").onclick = function() {
    if (!selectedOperation) {
      a = (+a) / 100
      outputElement.innerHTML = a
    } else {
      b = (+b) / 100
      outputElement.innerHTML = b
    }
  }
  
  document.getElementById("btn_op_sqrt").onclick = function() {
    if (!selectedOperation) {
      a = Math.sqrt(+a)
      outputElement.innerHTML = a
    } else {
      b = Math.sqrt(+b)
      outputElement.innerHTML = b
    }
  }
  
  document.getElementById("btn_op_pow").onclick = function() {
    if (!selectedOperation) {
      a = (+a) * (+a)
      outputElement.innerHTML = a
    } else {
      b = (+b) * (+b)
      outputElement.innerHTML = b
    }
  }
  
  document.getElementById("btn_op_factorial").onclick = function() {
    if (!selectedOperation) {
      let result = 1
      for (let i = 2; i <= (+a); i++) {
        result *= i
      }
      a = result
      outputElement.innerHTML = a
    } else {
      let result = 1
      for (let i = 2; i <= (+b); i++) {
        result *= i
      }
      b = result
      outputElement.innerHTML = b
    }
  }
  
  document.getElementById("btn_op_k").onclick = function() {
    if (!selectedOperation) {
      a = (+a) * 1000
      outputElement.innerHTML = a
    } else {
      b = (+b) * 1000
      outputElement.innerHTML = b
    }
  }
  
  document.getElementById('btn_op_resultcolorchange').onclick = function() {
    if (document.getElementById('result').style.background === 'gray') {
        document.getElementById('result').style.background = 'white'
        document.getElementById('result').style.color = 'black'
    } else {
        document.getElementById('result').style.background = 'gray'
        document.getElementById('result').style.color = 'white'
    }
  };
  
  document.getElementById("btn_op_clear").onclick = function() { 
    a = ''
    b = ''
    selectedOperation = ''
    expressionResult = ''
    outputElement.innerHTML = 0
  }
  
  document.getElementById("btn_op_equal").onclick = function() { 
    if (a === '' || b === '' || !selectedOperation)
        return
        
    switch(selectedOperation) { 
        case 'x':
            expressionResult = (+a) * (+b)
            break;
        case '+':
            expressionResult = (+a) + (+b)
            break;
        case '-':
            expressionResult = (+a) - (+b)
            break;
        case '/':
            expressionResult = (+a) / (+b)
            break;
    }
    
    a = expressionResult.toString()
    
    outputElement.innerHTML = a
  }
  
  document.getElementById('theme').addEventListener('click', function() {
    const currentTheme = document.body.className;
    if (currentTheme === 'light-theme') {
        document.body.className = 'dark-theme';
    } else {
        document.body.className = 'light-theme';
    }
  });
  
  };
  
