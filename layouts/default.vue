<template>
<div>
 <v-app-bar >
   <v-spacer />
   
   <div v-if="$auth.loggedIn">
      <v-btn text large>Welcome User </v-btn>
     <v-btn text @click="$auth.logout()">Logout</v-btn>
   </div>

   <div v-else>
     flag = {{ $auth.user }}
     <v-btn text to="/login">Login</v-btn>
     <v-btn text to="/register">Register</v-btn>
     
   </div>
 </v-app-bar>

 <v-content>

   <nuxt/>
 </v-content>
</div>
</template>

<script>
export default {
 
}
</script>
