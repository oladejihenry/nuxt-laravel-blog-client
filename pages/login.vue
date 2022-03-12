<template>
  <a href="#" @click.prevent="login">Login</a>
</template>

<script>
export default {
  methods: {
    login(){
      // this.$auth.loginWith('laravelSanctum', {
      //   data: {
      //     email: 'heolad@hotmail.com',
      //     password: 'love2020'
      //   }
      // })
      this.$auth.loginWith('cookie', {
        data: {
          email: 'heolad@hotmail.com',
          password: 'love2020'
        }
      }).then(()=>
        this.$router.push('/')
      )
    }
  }
}
</script>