### html file #####
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <div class="container">
      <div class="calculator">
        <!-- 1. this code is for form -->
        <form>
          <div class="display">
            <!-- 2. We are using the input function to get the desired output -->
            <input type="text" name="display" />
          </div>
          <div>
            <!-- 3. this code is for buttons set of  "AC","DE",".","/" 
            we are using the operator -->
            <!-- 4. to give the unique color for the special characters -->
            <input
              type="button"
              value="C"
              onclick="display.value = '' "
              class="operator"
            />
            <input
              type="button"
              value="DE"
              onclick="display.value = display.value.toString().slice(0,-1)"
              class="operator"
            />
            <input
              type="button"
              value="."
              onclick="display.value += '.' "
              class="operator"
            />
            <input
              type="button"
              value="/"
              onclick="display.value += '/' "
              class="operator"
            />
          </div>
          <!-- 5. This code is for buttons set of "7","8","9","*" -->
          <div>
            <input type="button" value="7" onclick="display.value += '7' " />
            <input type="button" value="8" onclick="display.value += '8' " />
            <input type="button" value="9" onclick="display.value += '9' " />
            <input
              type="button"
              value="*"
              onclick="display.value += '*' "
              class="operator"
            />
          </div>
          <!-- 6. This code is for buttons set of "4","5","6","-"-->
          <div>
            <input type="button" value="4" onclick="display.value += '4' " />
            <input type="button" value="5" onclick="display.value += '5' " />
            <input type="button" value="6" onclick="display.value += '6' " />
            <input
              type="button"
              value="-"
              onclick="display.value += '-' "
              class="operator"
            />
          </div>
          <!-- 7. This code is for buttons set of "1","2","3","+" -->
          <div>
            <input type="button" value="1" onclick="display.value += '1' " />
            <input type="button" value="2" onclick="display.value += '2' " />
            <input type="button" value="3" onclick="display.value += '3' " />
            <input
              type="button"
              value="+"
              onclick="display.value += '+' "
              class="operator"
            />
          </div>
          <!-- 8. This code os for buttons set of "00","0",-->
          <div>
            <input type="button" value="00" onclick="display.value += '00' " />
            <input type="button" value="0" onclick="display.value += '0' " />
            <input
              type="button"
              value="="
              onclick="display.value =eval(display.value) "
              class="equal operator"
            />
          </div>
        </form>
      </div>
    </div>
  </body>
</html>


#### CSS FILE #####
* {
  margin: 0;
  padding: 0;
  font-family: "Poppins", Impact, Haettenschweiler, "Arial Narrow Bold",
    sans-serif;
  box-sizing: border-box;
}

.container {
  width: 100%;
  height: 100vh;
  background: #0be5b9;
  display: flex;
  align-items: center;
  justify-content: center;
}

.calculator {
  background: #b7ffbc;
  padding: 20px;
  border-radius: 10px;
}

.calculator form input {
  border: 0;
  outline: 0;
  width: 60px;
  height: 60px;
  border-radius: 10px;
  box-shadow: -8px -8px 15px rgba(255, 255, 255, 0.1),
    5px 5px 15px rgba(0, 0, 0, 0.2);
  background: transparent;
  font-size: 30px;
  color: #8b0000;
  cursor: pointer;
  margin: 10px;
}

form .display {
  display: flex;
  justify-content: flex-start;
  margin: 20px 0;
}

form .display input {
  text-align: right;
  flex: 1;
  font-size: 45px;
  box-shadow: none;
}

form input.equal {
  width: 145px;
}

form input.operator {
  color: #405044;
}

footer {
  background-color: #4682b4;
  text-align: center;
}

