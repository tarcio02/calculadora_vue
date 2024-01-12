<script setup>
    const props = defineProps(['operacao', 'num1', 'num2'])
</script>


<template>
        
        <div>
            <input @keyup="props.num1" required type="number" placeholder="Insira o número 1"/>
            <div class="operation">
                <p>Operador:</p>
            <select @change="props.operacao">
                <option value="+">+</option>
                <option value="-">-</option>
                <option value="*">*</option>
                <option value="/">/</option>
            </select>
        </div>
            <input @keyup="props.num2" required type="number" placeholder="Insira o número 2"/>
        </div>
</template>

<style scope>
.operation {
    border: solid black 1px;
    max-width: 50%;
    margin: 0 auto;
    padding-bottom: 4px;
}
    input {
        margin: 30px;
        padding: 4px;
        border-radius: 4px;
        border: none;
    }
    select {
        background-color: gray;
        border: none;
    }
    p{
        margin-bottom: 0;
    }
</style>