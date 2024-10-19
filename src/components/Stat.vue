<script>
    import Text from './Text.vue';

    export default {
       props: {
        content: {
            type: String,
            required: true
        }
       } 
    }
</script>

<template>
    <div>
        <p>
            {{ content }}
        </p>
        <div>
            <Text :value="{text: 'YTD', number: '1.7bn'}"/>
        </div>
    </div>
</template>

<style>

</style>