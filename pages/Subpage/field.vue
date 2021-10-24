<template>
  <div class="Herd">
  <div class="Data" >
    <v-sheet class="Hdata" color="#AE78D6" elevation="4" height="50" rounded width="280" style='font-size: 20px; '>
    ข้อมูลบุคลากร</v-sheet>
   
    </div>
    <div>
    <div class="Hto">
        <h1 class="p-1 m-1 w-1/1 h-full" style='font-size: 18px; '>บุคลากรสายวิชาการ</h1>
        </div>
          </div>                          
          <v-btn block depressed elevation="1"  large plain style="height:4vh;">คอมพิวเตอร์ธุรกิจ</v-btn>
          <v-btn block depressed elevation="1"  large plain style="height:4vh;">เทคโนโลยีสารสนเทศ</v-btn>
          <v-btn block depressed elevation="1"  large plain style="height:4vh;">วิทยาการคอมพิวเตอร์</v-btn>
          <v-btn block depressed elevation="1"  large plain style="height:4vh;">ภูมิสารสนเทศศาสตร์</v-btn>
          <v-btn block depressed elevation="1"  large plain style="height:4vh;">วิศวกรรมคอมพิวเตอร์</v-btn>
          <v-btn block depressed elevation="1"  large plain style="height:4vh;">วิศวกรรมซอฟต์แวร์</v-btn>
          <v-btn block depressed elevation="1"  large plain style="height:4vh;">วิศวกรรมสารสนเทศและการสื่อสาร</v-btn>
          <v-btn block depressed elevation="1"  large plain style="height:4vh;">คอมพิวเตอร์กราฟิกและมัลติมีเดีย</v-btn>
                  
      <div>
    <div class="Htwo">
        <h1 class="p-1 m-1 w-1/1 h-full"  style='font-size: 18px; '>บุคลากรสายสนับสนุน</h1>
        </div>
          </div>                          
          <v-btn block depressed elevation="1" large plain style="height:4vh;">งานบริหารทั่วไป</v-btn>
          <v-btn block depressed elevation="1" large plain style="height:4vh;">งานวิชาการ</v-btn>
          <v-btn block depressed elevation="1" large plain style="height:4vh;">งานแผนงาน</v-btn>
          <v-btn block depressed elevation="1" large plain style="height:4vh;">งานปฏิบัติการ</v-btn>

    
  
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
.Htwo{
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