<template>
  <div class="login-form">
    <input v-model="username" placeholder="Username" type="text" />
    <input v-model="password" placeholder="Password" type="password" />
    <button @click="login">Login</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      username: '',
      password: '',
    };
  },
  methods: {
    login() {
      // Handle login logic
    },
  },
}
</script>

<style scoped>
/* Add your styles here */
</style>
