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
        align-items: center;
        width: 80%;
        margin-bottom: 10px;
        padding-left: 10px;
        padding-right: 10px;
        background-color: rgb(112, 72, 136);
        color: white;
        border-radius: 5%;
    }
</style>