<script setup>
import {ref} from "vue";
import {useAuthStore} from "../stores/auth.js";

const authStore = useAuthStore()


const form = ref({
  email: '',
  password: ''
})

</script>

<template>
  <div>
    <form @submit.prevent="authStore.handleLogin(form)"></form>
  </div>
</template>