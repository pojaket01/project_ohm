<template>
  <div>

    <div class="d-flex flex-row">
        <div class="p-0 m-0 w-1/4 h-full  "> 
            <v-sheet class="p-1 m-1 w-3/4 h-full" color="white" elevation="3" height="76vh" width="23vw" >
                <div class="p-0 m-0 w-3/4 h-full border-5 line rounded " style="height:75vh; width:22.5vw;border: 2px solid #2F528F; ">
                    
                </div>
                        </v-sheet>
        </div>
                
                    <v-sheet class="p-1 m-1 w-3/4 h-full" color="white" elevation="3"  height="76vh" width="74.5vw" >
                        <div class=" p-0 m-0 w-3/4 h-full  border-3 line rounded " style="width:74vw; height:75vh; width:74vw;border: 2px solid #2F528F; ">
                            </div>  
                                </v-sheet>
                           
        </div>
    </div>

</template>

<script>
import Outstanding from '../../components/Pages/Outstanding.vue'
import Developmentbudget from '../Subpage/developmentbudget.vue'
import field from '../Subpage/field.vue'
import Fieldstudy from '../Subpage/field.vue'
import Lastudy from '../Subpage/lastudy.vue'
import Powerrating from '../Subpage/powerrating.vue'
import seework from '../Subpage/seework.vue'
import outstandingpersonel from '../Subpage/outstandingpersonel.vue'
import Actionstatus from '../Subpage/actionstatus.vue'
import Documentation from '../Subpage/documentation.vue'
import Incumbent from '../Subpage/incumbent.vue'
import Developmentplan from '../Subpage/developmentplan.vue'
import Performancereport from '../Subpage/performancereport.vue'
export default {
  components: { field, Powerrating, seework, Developmentbudget, Lastudy ,outstandingpersonel, Actionstatus, Documentation, Incumbent, Developmentplan, Performancereport},

}
</script>

<style>

</style>