<template>
  <div>
    <v-app>
      <v-app-bar
        app
        color="#1134A6"
        dark
      >
        <v-spacer></v-spacer>
        <v-btn
          text
          @click="goToHome()"
          class="nav-button"
        >
          หน้าแรก
        </v-btn>
        <v-btn
          text
          @click="goToPageTwo()"
          class="nav-button"
        >
          ตารางเวลารถโดยสาร
        </v-btn>
        <v-btn
          text
          @click="goToPageThree()"
          class="nav-button"
        >
          ข้อมูลรถโดยสาร
        </v-btn>
      </v-app-bar>

      <v-main>
      <transition name="fade-transition" mode="out-in">
  <router-view />
</transition>


    </v-main>

    <!-- Footer -->
    <v-footer dark padless>
      <v-card class="flex" flat tile>
        <v-card-title class="teal" style="font-size: 20px;">
          <strong class="subheading" >Created by Arinrada Songyam</strong>
          <v-spacer></v-spacer>
          <!-- เพิ่มลิงค์ให้กับไอคอน -->
          Contact: 6410210688@psu.ac.th Tel. 083-424-757
        </v-card-title>
        <v-card-text class="py-2 white--text text-center">
          {{ new Date().getFullYear() }} — <strong>Department of Computer Science, Faculty of Science, Prince of Songkla University</strong>
        </v-card-text>
      </v-card>
    </v-footer>
  </v-app>
  </div>
</template>

<style lang="scss">
.nav-button {
  transition: all 0.3s; 
}

.nav-button:hover {
  transform: scale(1.1); 
}

.page-fade-enter-active, .page-fade-leave-active {
  transition: opacity 0.5s;
}

.page-fade-enter, .page-fade-leave-to {
  opacity: 0;
}
.page-expandX-enter-active, .page-expandX-leave-active {
  transition: transform 0.7s;
}

.page-expandX-enter, .page-expandX-leave-to {
  transform: scaleX(0);
}

</style>

<script>
export default {
  name: 'App',

  data: () => ({
    //
  }),
  methods: {
    goToHome() {
      this.$router.push({ path: '/' }).catch(() => {});
    },
    goToPageTwo() {
      this.$router.push({ path: '/busdetable' }).catch(() => {});
    },
    goToPageThree() {
      this.$router.push({ path: '/busdetail' }).catch(() => {});
    },
  },
};
</script>
