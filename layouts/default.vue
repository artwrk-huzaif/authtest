<template>
<div>
 <v-app-bar>
   <v-spacer />
   <div v-if="$auth.loggedIn">
     <v-btn text>Logout</v-btn>
   </div>

   <div v-else>
     {{ $auth.user }}
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
