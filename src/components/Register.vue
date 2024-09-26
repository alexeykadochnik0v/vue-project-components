<template>
    <div>
        <h2>Регистрация</h2>
        <UserProfile v-if="isLogin" />
        <LoginForm v-else/>
        <button @click="toggleLogin">{{ isLogin ? 'Выйти': 'Войти' }}</button>
    </div>
</template>

<script>
import LoginForm from './LoginForm.vue';
import UserProfile from './UserProfile.vue'
import { ref } from 'vue';
export default {
    components: {
        UserProfile,
        LoginForm
    },
    setup () {
        const isLogin = ref(false);

        const toggleLogin = () => {
            isLogin.value = !isLogin.value; // возвращает true или false
        }
  
        return {
            isLogin,
            toggleLogin
        }
    }
}
</script>

<style lang="scss" scoped>

</style>