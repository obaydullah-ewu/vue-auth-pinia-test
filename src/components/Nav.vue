<script setup>
import { useAuthStore} from "../stores/auth.js";
const authStore = useAuthStore()

</script>

<template>
  <div v-if="!authStore.user">
    Register
  </div>
  <div v-else>
    <button @click="authStore.handleLogout">Logout</button>
  </div>
</template>