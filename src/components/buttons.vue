<script setup>

</script>

<template>
    <div id="buttons-container">
        <button id="btn-comand" @change="props.comands">CE</button>
        <button id="btn-comand" @change="props.comands">C</button>
        <button id="btn-operator" @change="props.operator">/</button>
        <button class="number">7</button>
        <button class="number">8</button>
        <button class="number">9</button>
        <button id="btn-operator" @change="props.operator">*</button>
        <button class="number">4</button>
        <button class="number">5</button>
        <button class="number">6</button>
        <button id="btn-operator" @change="props.operator">-</button>
        <button class="number">1</button>
        <button class="number">2</button>
        <button class="number">3</button>
        <button id="btn-operator" @change="props.operator">+</button>
        <button id="btn-2fr" class="number">0</button>
        <button class="number">.</button>
        <!-- foi retirado o botão de igualdade devido ele ser desnecessário para esse projeto 
        <button id="equal-btn">=</button> -->
    </div>
</template>

<style scoped>
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

#buttons-container #btn-2fr {
    grid-column: span 2;
}


#buttons-container #btn-comand {
    grid-column: span 2;
    background-color: #eb5f40;
}

#buttons-container #btn-comand:hover {
    background-color: #e4482c;
}

#buttons-container #btn-operator {
    background-color: #75a5cb;
}

#buttons-container #btn-operator:hover {
    background-color: #3a91d8;
}


/* foi retirado o botão de igualdade devido ele ser desnecessário para esse projeto
#buttons-container #equal-btn {
    grid-column: span 2;
    background-color: #75a5cb;
}

#buttons-container #equal-btn:hover {
    background-color: #3a91d8;
} */

</style>