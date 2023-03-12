<script setup>
import {ref} from "vue";
import {useAuthStore} from "../stores/auth.js";
import { useRoute } from "vue-router";

const route = useRoute();
const authStore = useAuthStore()
const form = ref({
  token: route.params.token,
  email: route.query.email,
  password: '',
  password_confirmation: ''
})


</script>

<template>
  <template>
    <div>
      <form @submit.prevent="authStore.handleResetPassword(form)"></form>
    </div>
  </template>

</template>