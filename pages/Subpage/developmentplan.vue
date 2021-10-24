<template>
  <div class="Herd">
  <div class="Data" >
    <v-sheet class="Hdata" color="#AE78D6" elevation="4" height="50" rounded width="300" style='font-size: 20px; '>
    แผนพัฒนาบุคลากร</v-sheet>
   
    </div>
    <div>
    <div class="Hto">
        </div>
          </div>                          
          <v-btn block depressed elevation="1"  large plain style="height:4vh;">2554-2557</v-btn>
          <v-btn block depressed elevation="1"  large plain style="height:4vh;">2559-2562</v-btn>
          <v-btn block depressed elevation="1"  large plain style="height:4vh;">2563-2566</v-btn>

                  
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