<template>
  <div class="container">
    <h1>ค้นหาการเดินทางที่ต้องการจะไป</h1>

    <label class="custom-label">ตอนนี้คุณอยู่ที่</label>
    <v-select v-model="start" :items="items" label="คุณอยู่ตรงนี้" outlined></v-select>

    <label class="custom-label">ไปยัง</label>
    <v-select v-model="stop" :items="items" label="คุณจะไปที่นี่" outlined></v-select>

    <v-btn color="green" dark class="mb-2" block @click="searchRoute">ค้นหา</v-btn>

    <div v-if="selectedRoute">
      <h2>เส้นทาง: {{ selectedRoute.start }} ถึง {{ selectedRoute.stop }}</h2>
      <p>ชื่อสายรถ: {{ selectedRoute.busName }}</p>
      <img :src="imagePath" alt="รูปภาพเส้นทาง" />
    </div>

   
    <v-alert v-if="showErrorAlert" type="error" dismissible>
      ไม่พบเส้นทางเดินรถ
    </v-alert>
  </div>
</template>

<script>
import axios from 'axios';

export default {
  data() {
    return {
      items: ['A', 'B', 'C', 'D', 'E'],
      start: null,
      stop: null,
      selectedRoute: null,
      imagePath: null,
      showErrorAlert: false, 
  }
},
methods: {
  async searchRoute() {
  if (this.start && this.stop) {
    try {
      this.imagePath = null; // เพิ่มบรรทัดนี้เพื่อลบภาพเก่า

      const response = await axios.get(`http://localhost:9000/find?start=${this.start}&stop=${this.stop}`);
      if (response.data.length > 0) {
        this.selectedRoute = response.data[0];
        this.imagePath = this.selectedRoute.link;

        if (this.start === "A" && this.stop === "B") {
  this.selectedRoute.busName = "สายที่ 1";
} else if (this.start === "B" && this.stop === "C") {
  this.selectedRoute.busName = "สายที่ 1";
} else if (this.start === "D" && this.stop === "E") {
  this.selectedRoute.busName = "สายที่ 1";
} else if (this.start === "E" && this.stop === "A") {
  this.selectedRoute.busName = "สายที่ 1";
} else if (this.start === "A" && this.stop === "C") {
  this.selectedRoute.busName = "สายที่ 2";
} else if (this.start === "A" && this.stop === "E") {
  this.selectedRoute.busName = "สายที่ 2";
} else if (this.start === "B" && this.stop === "E") {
  this.selectedRoute.busName = "สายที่ 3";
} else if (this.start === "C" && this.stop === "D") {
  this.selectedRoute.busName = "สายที่ 1 และ สายที่ 2";
} else if (this.start === "D" && this.stop === "E") {
  this.selectedRoute.busName = "สายที่ 1 และ สายที่ 2";
} else if (this.start === "A" && this.stop === "E") {
  this.selectedRoute.busName = "สายที่ 2 และ สายที่ 3";
} else {
  this.selectedRoute.busName = "สายอื่น ๆ"; // สายรถอื่น ๆ ที่คุณต้องการกำหนดเงื่อนไข
}

this.showErrorAlert = false;
      } else {
        this.selectedRoute = null;
        this.imagePath = null; // เพิ่มบรรทัดนี้เพื่อลบภาพเก่า
        this.showErrorAlert = true;
      }
    } catch (error) {
      console.error(error.message);
      this.showErrorAlert = true;
    }
  }
},
  },
};
</script>

<style>
.custom-label {
  font-size: 18px;
  font-family: 'SarabanPSK', sans-serif;
}
img {
  max-width: 100%;
  height: auto;
  border: 1px solid #ddd;
  border-radius: 8px;
  box-shadow: 0 0 5px rgba(0, 0, 0, 0.2);
  margin: 20px 0;
}

/* จัดหน้าเว็บ */
.container {
  max-width: 800px;
  margin: 0 auto;
  padding: 20px;
  background-color: #f9f9f9;
  border: 1px solid #ddd;
  border-radius: 8px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
}
</style>