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

    methods:{
        loginUser(userinfo){
            debugger
            alert('You Pressed Button')
        }
    }

}
</script>

<style>

</style>