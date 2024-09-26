<template>
    <div>
        <button :disabled="count <= 1" @click="decrement">-</button>
        {{ count }}
        <button  @click="increment">+</button>
    </div>
</template>

<script>
import { ref } from 'vue';
export default {
    setup () {
        const count = ref(1);

        const increment = () => {
            count.value++;
        }

        const decrement = () => {
           if (count.value > 1) {
            count.value--;
           }
        }

        return {
            count,
            increment,
            decrement
        }
    }
}
</script>

<style lang="scss" scoped>

</style>