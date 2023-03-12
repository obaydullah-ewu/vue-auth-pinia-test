<script setup>
import {  onMounted } from 'vue'
import { useAuthStore} from "../stores/auth.js";

const authStore = useAuthStore()

onMounted(async () => {
  await authStore.getToken()
})
</script>

<template>
  <div v-if="authStore.user">
    <h1>{{ authStore.user?.name}}</h1>
    <h1>{{ authStore.user?.email}}</h1>
  </div>
  <div v-else>
    <h1>Go and Login</h1>
  </div>

</template>
