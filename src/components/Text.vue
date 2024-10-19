<script>
    export default {
       props: {
        value: {
            type: Object,
            required: true
        },
       } 
    }
</script>

<template>
    <div className="text-container">
        <p>
            {{ value.text }}
        </p>
        <p>
            {{ value.number }}
        </p>
    </div>
</template>

<style>
    .text-container {
        display: flex;
        justify-content: space-between;
        padding: 25px;
        align-items: center;
        width: 80%;
        padding: 10px 10px 10px 10px;
        background-color: rgb(112, 72, 136);
        color: white;
    }
</style>