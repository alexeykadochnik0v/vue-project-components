<template>
    <div>
        <input type="text" v-model="inputText">
        <p v-if="inputText === ''">Нужно заполнить поле ввода</p>
        <p v-else>Поле ввода не пустое</p>
    </div>
</template>

<script>
export default {
    data () {
        return {
            inputText: '',
        }
    },
    setup () {
        

        return {}
    }
}
</script>

<style lang="scss" scoped>

</style>