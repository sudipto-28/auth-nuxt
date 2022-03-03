<template>
<div class="">
  <h1>Account</h1>
  <button @click="logout">Logout</button>
</div>

</template>

<script>
export default {
  middleware: 'auth',
  methods: {
    async logout() {
      console.log('Logout')
      await this.$auth.logout()
      console.log('this.$auth', this.$auth)
    }
  }
}
</script>

<style>

</style>
