<script setup>
import { reactive } from 'vue';

const previusOperationText = document.querySelector("#previous-operation");
const currentOperationText = document.querySelector("#current-operation");
const buttons = document.querySelectorAll("#buttons-container button");

class Calculator {

} 

buttons.forEach((btn) => {

  btn.addEventListener("click", (e) => {
    const value = e.target.innerText;

    console.log(value);
  });

});


</script>

<template>
<body>
  <div id="calc">
  <h3>Calculadora</h3>
  <div id="operations">
    <div id="previus-operation"></div>
    <div id="current-operation"></div>
  </div>
  <div id="buttons-container">
    <button>CE</button>
    <button>C</button>
    <button>DEL</button>
    <button>/</button>
    <button class="number">7</button>
    <button class="number">8</button>
    <button class="number">9</button>
    <button>*</button>
    <button class="number">4</button>
    <button class="number">5</button>
    <button class="number">6</button>
    <button>-</button>
    <button class="number">1</button>
    <button class="number">2</button>
    <button class="number">3</button>
    <button>+</button>
    <button class="number">0</button>
    <button class="number">.</button>
    <button id="equal-btn">=</button>
  </div>
</div>
</body>
</template>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: Arial, Helvetica, sans-serif;
}
body {
  height: 100vh;
  background-color: #333;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 3em;
}

#calc {
  width: 400px;
  padding: 0.5em;
  background-color: #c4c4c4;
  color: #000;
  display: flex;
  flex-direction: column;
}

#calc h3 {
  font-size: .8em;
  font-weight: 300;
  color: #666;
}

#operations {
  text-align: right;
}

#current-operation,
#previus-operation {
  min-height: 1.6em;
  padding: 0.2em;
  overflow-wrap: break-word;
}

#previus-operation {
  color: #777;
}

#current-operation {
  font-size: 3em;
  font-weight: 700;
}

#buttons-container {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr;
  gap: 3px;
  }

  #buttons-container button {
    border: 1px solid transparent;
    border-radius: 0;
    height: 4em;
    font-size: 1.2em;
    background-color: #dbdbdb;
    cursor: pointer;
  }

  #buttons-container .number {
    background-color: #f3f3f3;
  }

  #buttons-container button:hover {
    background-color: #bababa;
    border-color: #999;
  }

  #buttons-container #equal-btn {
    grid-column: span 2;
    background-color: #75a5cb;
  }

  #buttons-container #equal-btn:hover {
    background-color: #3a91d8;
  }
</style>
