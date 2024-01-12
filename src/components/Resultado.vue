<script setup>
    const props = defineProps(['num1', 'num2', 'result'])
</script>


<template>
    <span v-if="props.num1 && props.num2 !=''"><h2>Resultado: {{ props.result }}</h2></span>
    <span v-else-if="props.num1 || props.num2 === ''"><h2>Digite dois valores</h2></span>
</template>

<style scoped>
    span h2{
        color: white;
        background-color: black;
        padding-bottom:20px;
        padding-top: 20px;
    }
</style>
