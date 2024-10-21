<script>
    export default{ 
        props: {
            visible: {
                type: Boolean,
                required: true
            },
            content: {
                type: String
            }
        },
        data () {
            return {
                statInfo: {
                    'Retail Value': 'Some text for Retail Value',
                    'COGS Value': 'Some text for COGS Value',
                    'CO2 Emissions': 'Some text for CO2 Emissions',
                    'Fail Rate': 'Some text for Fail Rate',
                    'Failed Retail Value': 'Some text for Failed Retail Value'
                }
            }
        }
    }
</script>
<template>
    <div :class="visible ? `stat-info + stat-info__visible` : 'stat-info'">
        <p className="info-text">
            {{ statInfo[content] }}
        </p>
    </div>
</template>
<style>
    .stat-info {
        width: 99%;
        background-color: rgb(124, 82, 158);
        height: 100px;
        visibility: hidden;
        border-radius: 10px;
        margin: 5px;
        display: flex;
        justify-content: center;
    }
    .stat-info__visible {
        visibility: visible;
    }
    .info-text {
        color: white;
    }
</style>