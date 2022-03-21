<template>
  <v-app-bar fixed >
      <a href="/"> <v-img
  max-height="100"
  max-width="100"
  src="../assets/logo_voice_manager.png"
  id="logo"
></v-img>
</a>

      <v-toolbar-title>VOICE MANAGER</v-toolbar-title>
      <v-spacer></v-spacer>
 <v-spacer></v-spacer>
    
  </v-app-bar>
</template>

<script>

// import axios from'axios'
export default {
    name:'Header',
     data:() => ( {
    
  }),
  
   
}
</script>

<style>
#logo{
    margin-right: 2%;
}
</style>