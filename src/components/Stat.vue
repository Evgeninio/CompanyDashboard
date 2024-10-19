<script>
    import Text from './Text.vue';

    export default {
       props: {
        content: {
            type: String,
            required: true
        }
       },
       components: { Text },
       data() {
        return {
            value: {
                'Retail Value': {
                    'YTD': '1.7bn',
                    'MTD': '7.5M'
                },
                'COGS Value': {
                    'YTD': '225.4M',
                    'MTD': '13.6M'
                },
                'CO2 Emissions': {
                    'YTD': '590.1K',
                    'MTD': '42.3K'
                },
                'Fail Rate': {
                    'YTD': '7.6 %',
                    'MTD': '5.0 %'
                },
                'Failed Retail Value': {
                    'YTD': '78.1M',
                    'MTD': '553.6K'
                }
            }
        } 
       },
       methods: {
        handleMouseEnter() {
            const textContent = this.$refs.statElement.textContent;
            this.$emit('stat-hover', textContent)
        },
        handleMouseLeave() {
            this.$emit('stat-hover', null)
        }
    }
    }
</script>

<template>
    <div className="stat">
        <p class="stat-title" ref="statElement" @mouseenter="handleMouseEnter" @mouseleave="handleMouseLeave">
            {{ content }}
        </p>
        <div className="stat-value">
            <Text :value="{text: 'YTD', number: value[content]['YTD']}" />
            <Text :value="{text: 'MTD', number: value[content]['MTD']}"/>
        </div>
    </div>
</template>

<style>
    .stat {
        display: flex;
        flex-direction: column;
        background-color: rgb(87, 46, 122);
        border-radius: 5%;
        width: 13%;
        justify-content: center;
        align-items: center;

    }
    .stat-title {
        color: white;
        padding-left: 15px;
        letter-spacing: 1px;
        font-weight: 1000;
        font-size: 22px;
        font-family: 'Courier New', Courier, monospace;
        white-space: pre-wrap;
        align-self: self-start;
        padding-left: 25px;

    }
    .stat-value {
        display: flex;
        align-items: center;
        flex-direction: column;
        gap: 5px;
        width: 80%;
        padding-bottom: 10px;
    }
</style>