<script>
    export default {
        props: {
            content: {
                type: String,
                required: true
            }
        },
        methods: {
                handleTest () {
                alert('Hello')
            }
        }
    }
</script>

<template>
    <button className="header-button" @click="handleTest()">
        <p> {{ content }}</p>
    </button>
</template>

<style scoped>
    .header-button {
        background-color: rgba(124, 82, 158, 0.8); 
        color: rgba(255, 255, 255, 0.6);
        font-family:Georgia, 'Times New Roman', Times, serif;
        border: 0;
        border-radius: 10px;
        letter-spacing: 1px;
        font-size: 10px;
        font-weight: bold;
        text-transform: uppercase;
        cursor: pointer;
        transition: background-color 0.3s ease;
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        min-width: 20%;
    }
</style>