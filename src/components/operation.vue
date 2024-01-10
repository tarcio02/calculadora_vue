<script setup>
    
</script>

<template>

<div id="operations">
    <div class="nums">
        <div id="num1"> 15</div>
        <div id="num2"> +56</div>
    </div>
    <div id="result"> </div>
</div>

</template>

<style scoped>

#operations {
    text-align: right;
}

.nums {
    display: flex;
}

#result,
#num1,
#num2{
    min-height: 1.6em;
    padding: 0.2em;
    overflow-wrap: break-word;
}

#num1,
#num2{
    color: #777;
    max-width: 50%;
    width: 100%;
}

#result {
    font-size: 3em;
    font-weight: 700;
}
</style>