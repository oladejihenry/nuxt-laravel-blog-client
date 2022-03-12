<template>
  <a href="#" @click.prevent="login">Login</a>
</template>

<script>
export default {
  methods: {
    login(event){
      this.$auth.loginWith('cookie', {
        data: {
          email: 'heolad@gmail.com',
          password: 'love2020'
        }
      })
    }
  }
}
</script>