<template>
  <v-container>
     <h1> Login </h1>
    <UserAuthForm buttonText="Login" :submitForm="loginUser" />
  </v-container>
</template>

<script>
import UserAuthForm from '@/components/UserAuthForm'
export default {
    components:{
        UserAuthForm
    },

  methods: {
    async loginUser(userinfo) {
        
      try {
        let response = await this.$auth.loginWith('local', { data: userinfo })
        console.log(response)
      } catch (err) {
        console.log(err)
      }
    }
  }

}
</script>

<style>

</style>