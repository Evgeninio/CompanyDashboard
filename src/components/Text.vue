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
        <p className="text-title">
            {{ value.text }}
        </p>
        <p className="text-number">
            {{ value.number }}
        </p>
    </div>
</template>

<style>
    .text-container {
        display: flex;
        justify-content: space-between;
        align-items: center;
        width: 100%;
        gap: 50px;
        margin: 5px 0;
        padding-left: 10px;
        padding-right: 10px;
        background-color: rgb(112, 72, 136);
        color: white;
        border-radius: 5px;

    }
    .text-title {
        color: rgba(255, 255, 255, 0.8);
    }
    .text-number {
        font-weight: 1000;
        font-family: 'Courier New', Courier, monospace;
    }
</style>