<template>
    <v-container>
      
      <v-row>
          <v-col clos="12">
          <BusDetail/>
      </v-col>
      </v-row>
    </v-container>
  </template>
  
  <script>
  export default {
      components:{
        BusDetail: () => import('../components/BusDetail.vue')
      }
  }   
  </script>
  
  <style>
  
  </style>