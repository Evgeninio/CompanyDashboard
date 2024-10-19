<script>
    import Stat from './Stat.vue';

    export default {
        components: { Stat },
    }
</script>

<template>
    <div className="stats-list">
        <Stat :content="'Retail Value'"/>
        <Stat :content="'Retail Value'"/>
        <Stat :content="'Retail Value'"/>
        <Stat :content="'Retail Value'"/>
        <Stat :content="'Retail Value'"/>
    </div>
</template>

<style>
    .stats-list {
        display: flex;
        gap: 50px;
        border-radius: 5%;
        margin-left: 20px;
        justify-content: space-between;
    }
</style>