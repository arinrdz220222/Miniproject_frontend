<template>
  <div>
    <div class="header">
      <h1 class="title">ตารางเวลารถออก</h1>
      <p class="subtitle">รถโดยสารประจำทางภายในมหาวิทยาลัยประกอบไปด้วย 3 สายได้แก่ สายที่ 1, สายที่ 2 และสายที่ 3 ซึ่งเป็นรถขนส่งมวลชนให้บริการฟรีทุกวันไม่เว้นวันหยุดราชการ</p>
    </div>
    <v-row>
   
      <v-col class="hover-card">
        <v-card-title>
          แผนที่เส้นทางรถโดยสารทั้งหมด
        </v-card-title>
        <div>
          <v-card max-height="620" max-width="350" style="box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.8); margin-top: 20px;">
            <v-img src="../assets/busline/4.jpg" height="600px"></v-img>
          </v-card>
        </div>
      </v-col>
    
      <v-col class="hover-card">
        <v-card-title>
          แผนที่เส้นทางรถโดยสารสายที่ 1
        </v-card-title>
        <v-card-subtitle>
          (สายสีเขียว)
        </v-card-subtitle>
        <v-expand-transition>
          <div>
            <v-card max-height="600" max-width="350" style="box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.8);">
              <v-img src="../assets/busline/5.jpg" height="600px"></v-img>
            </v-card>
          </div>
        </v-expand-transition>
      </v-col>


      <v-col class="hover-card">
        <v-card-title>
          แผนที่เส้นทางรถโดยสารสายที่ 2
        </v-card-title>
        <v-card-subtitle>
          (สายสีส้ม)
        </v-card-subtitle>
        <v-expand-transition>
          <div>
            <v-card max-height="600" max-width="350" style="box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.8);">
              <v-img src="../assets/busline/6.jpg" height="600px"></v-img>
            </v-card>
          </div>
        </v-expand-transition>
      </v-col>

     
      <v-col class="hover-card">
        <v-card-title>
          แผนที่เส้นทางรถโดยสารสายที่ 3
        </v-card-title>
        <v-card-subtitle>
          (สายสีน้ำเงิน)
        </v-card-subtitle>
        <v-expand-transition>
          <div>
            <v-card max-height="600" max-width="350" style="box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.8);">
              <v-img src="../assets/busline/7.jpg" height="600px"></v-img>
            </v-card>
          </div>
        </v-expand-transition>
      </v-col>
    </v-row>
  </div>
</template>


<script>
export default {
  data: () => ({
    show1: false,
    show2: false,
    show3: false,
  }),
};
</script>
<style scoped>



.title-frame-small h1 {
  font-size: 20px;
  margin: 0;
}
.hover-card {
  transition: transform 0.3s;
}

.hover-card:hover {
  transform: scale(1.05);
}
.header {
  background-color: #007BFF; 
  padding: 20px;
  text-align: center;
  color: #fff; 
  border-radius: 40px; 

}

.title {
  font-size: 200px;
  margin: 0;
}



</style>
