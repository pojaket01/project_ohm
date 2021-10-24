<template>
  <div class="Herd">
  <div class="Data" >
    <v-sheet class="Hdata" color="#AE78D6" elevation="4" height="50" rounded width="300" style='font-size: 18px; '>
    สถานะดำเนินการ
</v-sheet>
   
    </div>
    <div>
    <div class="Hto">
        </div>
          </div>                          
          <v-btn block depressed elevation="1" x-large large plain style="height:4vh;">การขอประเมินผลการสอนฯ</v-btn>
          <v-btn block depressed elevation="1" x-large large plain style="height:4vh;">การขอกำหนดตำแหน่งทางวิชาการ</v-btn>            
      <div>
  
          </div>                          


  
     </div>
</template>

<script>
export default {

}
</script>

<style>
.Herd{
  display: flex;
  justify-content: center;
  flex-direction: column;
  
}
.Hto{
  display: flex;
  justify-content: center;
}

.Data{
    display: flex;
    justify-content: center;
}
.Hdata{
  margin: 5px;
  display: flex; 
  justify-content: center; 
  align-items: center;
  font-weight : bold;
} 
</style>