<script>
    import Stat from './Stat.vue';
    import StatInfo from './StatInfo.vue';
    export default {
        components: { Stat, StatInfo },
        data() {
            return {
                statsTitles: ['Retail Value', 'COGS Value',  'CO2 Emissions', 'Fail Rate', 'Failed Retail Value'],
                isVisible: false,
            }
        },
        methods: {
        handleMouse(visible) {
            this.isVisible = visible;
        },
        handleTitle(e) {
            console.log(e)
        }
    }
    }
</script>

<template>
    <div className="stats-list">
        <Stat v-for="(title, index) in statsTitles" :content="title" :index="index" @mouseenter="handleMouse(true)" @mouseleave="handleMouse(false)"/>
    </div>
    <div>
        <StatInfo :visible="isVisible"/>
    </div>
</template>

<style>
    .stats-list {
        display: flex;
        gap: 50px;
        border-radius: 5%;
        margin-left: 20px;
        margin-right: 20px;
        justify-content: space-between;
    }
</style>