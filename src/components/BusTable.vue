<template>
  <div>
    <div class="header">
      <p class="title">ตารางเวลารถออก</p>
    </div>
    <v-row>
     
      <v-col  class="hover-card">
        <v-card-title>
          สายที่ 1
        </v-card-title>
        <v-card-subtitle>
          ประกอบไปด้วยสถานี A, สถานี B, สถานี C, สถานี D, และสถานี E
 จำนวนรถทั้งหมด 6 คัน บริการทุกวันไม่เว้นหยุดราชการ
        </v-card-subtitle>
        
      
        <div>
          <v-card class="mx-auto" max-width="400" style="box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.8);">
            <v-img src="../assets/busline/3.jpg" height="650px"></v-img>
          </v-card>
        </div>
     
      
      </v-col>
     

    
      <v-col class="hover-card">
        <v-card-title>
          สายที่ 2
        </v-card-title>
        <v-card-subtitle>
          ประกอบไปด้วยสถานี A, สถานี C, สถานี D, และสถานี E
 จำนวนรถทั้งหมด 3 คัน บริการทุกวันไม่เว้นหยุดราชการ
        </v-card-subtitle>
        
        <v-expand-transition>
        <div>
          <v-card class="mx-auto" max-width="400" style="box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.8);">
            <v-img src="../assets/busline/1.jpg" height="650px"></v-img>
          </v-card>
        </div>
      </v-expand-transition>
      
      </v-col>

     
      
        <v-col  class="hover-card">
          <v-card-title>
            สายที่ 3
          </v-card-title>
          <v-card-subtitle>
            ประกอบไปด้วยสถานี A, สถานี B, และสถานี E
 จำนวนรถทั้งหมด 3 คัน บริการทุกวันไม่เว้นหยุดราชการ
          </v-card-subtitle>
         
          <v-expand-transition>
            <div >
              <v-card class="mx-auto" max-width="400" style="box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.8);">
                <v-img src="../assets/busline/2.jpg" height="600px"></v-img>
              </v-card>
            </div>
          </v-expand-transition>
        </v-col>
      </v-row>
      <br><br>
    <h2 class="h4">หมายเหตุ เวลา 07.30-09.00 น. เมื่อผู้โดยสายเต็มรถ ให้ออกรถทันที เว้นแต่ผู้โดยสารไม่เต็มรถให้ออกตามเวลา</h2>
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
  font-size: 48px; 
  margin: 0;
}

</style>
