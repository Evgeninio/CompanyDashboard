<script>
    import Stat from './Stat.vue';
    import StatInfo from './StatInfo.vue';
    export default {
        components: { Stat, StatInfo },
        data() {
            return {
                statsTitles: ['Retail Value', 'COGS Value',  'CO2 Emissions', 'Fail Rate', 'Failed Retail Value'],
                isVisible: false,
                title: ''
            }
        },
        methods: {
        handleStatHover(textContent) {
            this.title = textContent
            this.isVisible = !!textContent
        }
    }
    }
</script>

<template>
    <div className="stats-list">
        <Stat v-for="(title, index) in statsTitles" :content="title" :index="index" @stat-hover="handleStatHover" />
        <StatInfo :visible="isVisible" :content="title"/>
    </div>
    <div>

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
        flex-wrap: wrap;
        flex: 1 1 13%;
    }

    @media screen and (width >=1251px) and (width <=1500px) { 
        .stat{
            flex: 1 1 30%;
        }
        
    }

    @media screen and (width >=830px) and (width <=1250px){ 
        .stats-list{
            justify-content: center;
            flex: 1 1 45%;
        }
    }
    @media screen and (width <=829px){ 
        .stats-list {
            flex-direction: column;
        }
    }
</style>