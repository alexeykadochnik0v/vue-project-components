<template>
    <div>
        <p :style="{color: textColor}">Lorem ipsum dolor sit amet.</p>
        <!-- : аналогично v-bind -->
        <button @click="changeColor">Click button</button>
    </div>
</template>

<script>
export default {
    data () {
        return {
            textColor: 'red'
        }
    },
    methods: {
        changeColor () {
            this.textColor = (this.textColor ==='red') ? 'blue' : 'red'
        }
    },
    setup () {
        

        return {}
    }
}
</script>

<style lang="scss">

</style>