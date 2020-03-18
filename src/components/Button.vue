<template>
    <div id="kanye-button" @click='updateQuote'>
        <p >Click me for more Kanye!</p>
    </div>
</template>

<script>
    export default {
        methods: {
            updateQuote: function() {
                this.$root.$emit('newKanyeQuote')
            }
        }
    }
</script>

<style scoped>

</style>