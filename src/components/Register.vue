<script setup>
import {ref} from "vue";
import {useAuthStore} from "../stores/auth.js";

const authStore = useAuthStore()
const form = ref({
  name: '',
  email: '',
  password: '',
  password_confirmation: ''
})


</script>

<template>
  <template>
    <div>
      <form @submit.prevent="authStore.handleRegister(form)"></form>
    </div>
  </template>

</template>