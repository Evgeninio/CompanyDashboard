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
    }
</script>

<template>
    <div className="stat">
        <p class="stat-title">
            {{ content }}
        </p>
        <div className="stat-value">
            <Text :value="{text: 'YTD', number: '1.7bn'}"/>
            <Text :value="{text: 'YTD', number: '1.7bn'}"/>
        </div>
    </div>
</template>

<style>
    .stat {
        display: flex;
        flex-direction: column;
        background-color: rgb(87, 46, 122);
        min-width: 13%;
        border-radius: 5%;

    }
    .stat-title {
        color: white;
        padding-left: 20px;
        letter-spacing: 1px;
        font-weight: 1000;
        font-family: 'Courier New', Courier, monospace;
        font-size: large;
    }
    .stat-value {
        padding-left: 20px;
        display: flex;
        flex-direction: column;
        gap: 5px;
        align-self: self-start;
        width: 100%;
    }
</style>