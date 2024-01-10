<script setup>
import { reactive } from 'vue';
import operation from './components/operation.vue'
import buttons from './components/buttons.vue'

const estado = reactive ({
  operator: '',
  num1:'',
  num2: ''
});

const resultado = ()=> {
  const {operator} = estado
  switch(operator) {
    case'-':
    return parseFloat(estado.num1) - parseFloat(estado.num2)
    case'*':
    return parseFloat(estado.num1) * parseFloat(estado.num2)
    case'/':
    return parseFloat(estado.num1) / parseFloat(estado.num2)
    case'+':
    return  parseFloat(estado.num1) + parseFloat(estado.num2)
  }
}


</script>

<template>
<body>

  <div id="calc">
  <h3>Calculadora vue.js</h3>
  <operation/>
  <buttons/>
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

/* operations */

/* buttons */


</style>
