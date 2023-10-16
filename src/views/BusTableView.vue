<template>
  <v-container>
    <v-row>
      <v-col clos="12">
        <BusTable />
      </v-col>
    </v-row>
    
  </v-container>
</template>
  
  <script>
  export default {
      components:{
        BusTable: () => import('../components/BusTable.vue')
      }
  }   
  </script>
  
  <style>
  
  </style>