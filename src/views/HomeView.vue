<template>
 
  <v-row >
      <v-col class="x" clos="12">
        <HelloWorld />
  </v-col>
  </v-row>
  


</template>

<script>
import HelloWorld from '../components/HelloWorld.vue'

export default {
  name: 'Home',

  components: {
    HelloWorld
  }
}
</script>
<style>
.bak {
  background-image: url('@/assets/11.png');
  background-size: cover;
  height: 100vh; 
  width: 100%;
 
}
</style>