<script>
    import  HeaderButton  from './HeaderButton.vue'

    export default {
        name: "Header",
        components: { HeaderButton },
        data() {
            return {
                buttonTitles: ["Company", "Quality", "Sourcing", "Logistics", "Sustainability" ]
            }
        }
    }
</script>

<template>
    <div className="header">
        <p className="header-text">
            Company dashboard
        </p>
        <div className="header-buttons">
            <HeaderButton v-for="(title, index) in buttonTitles" :key="index" :content="title" />
        </div>
    </div>
</template>

<style scoped>
    .header {
        display: flex;
        justify-content: space-between;
        padding: 20px;
    }
    .header-text {
        color: white;
        font-family: 'Courier New', Courier, monospace;
        font-weight: 1000;
        font-size: 24px;
        letter-spacing: 1px;
        padding-left: 10px;
    }
    .header-buttons {
        min-width: 50%;
        display: flex;
        gap: 10px; 
        justify-content: center;
        padding: 20px;
        background-color: rgb(53, 2, 79);
    }
</style>
