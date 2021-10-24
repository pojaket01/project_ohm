<template>
<div class="d-flex mb-6 ">
    <div class="d-flex justify-content: flex-start;">
        <img src="@/assets/New.PNG" alt="" width="90%">
    </div>

    <div class="d-block widtter">
        <div class="d-flex justify-end">
            <div class="d-flex align-center mr-5 ">
                <p style="margin-right: 17rem; margin-top: 1.50rem;">ผู้ใช้งาน : </p>
            </div>
            <div>
                <v-btn  @click.prevent="logout()" large x-large x-small style="margin-top: 0.50rem;">ออกจากระบบ</v-btn>
            </div>
        </div>

        <div class="Hd" style="display: flex; width: 100%; height: 53%; justify-content: flex-end; align-items: center;">
            <div class="Box" style="display: flex; width: 95%;">
                <v-app-bar class="display: flex; justify-content: space-between" color="#AE78D6" dense dark>
                    <div class="text-center ">
                        <v-menu offset-y>
                            <template v-slot:activator="{ on, attrs }">
                                <v-btn color="#AE78D6" dark v-bind="attrs" v-on="on" style="width: 165%;">
                                    ข้อมูลบุคลากร
                                    <!-- <pre> {{ContactTabinformation}} </pre> -->
                                </v-btn>
                            </template>
                            <v-list>
                                <v-list-item v-for="(infimationtab, index) in information" :key="infimationtab.id" @click="informationState = index" :class="{active: informationState === index}">
                                    <v-list-item-title>{{ infimationtab }}</v-list-item-title>
                                </v-list-item>
                            </v-list>
                        </v-menu>
                    </div>

                    <div class="text-center">
                        <v-menu offset-y>
                            <template v-slot:activator="{ on, attrs }">
                                <v-btn color="#AE78D6" dark v-bind="attrs" v-on="on" style="width: 150%;">
                                    การพัฒนาตนเอง
                                    <!-- <pre> {{ContactTabdevelopment}} </pre> -->
                                </v-btn>
                            </template>
                            <v-list>
                                <v-list-item v-for="(developmenttab, index) in development" :key="developmenttab.id" @click="developmentState = index" :class="{active: developmentState === index}">
                                    <v-list-item-title>{{ developmenttab }}</v-list-item-title>
                                </v-list-item>
                            </v-list>
                        </v-menu>
                    </div>

                    <div class="text-center">
                        <v-menu offset-y>
                            <template v-slot:activator="{ on, attrs }">
                                <v-btn color="#AE78D6" dark v-bind="attrs" v-on="on" style="width: 140%;">
                                    ตำแหน่งทางวิชาการ
                                    <!-- <pre> {{ContactTabposition}} </pre> -->
                                </v-btn>
                            </template>
                            <v-list>
                                <v-list-item v-for="(positiontab, index) in position" :key="positiontab.id" @click="positionState = index" :class="{active: positionState === index}">
                                    <v-list-item-title>{{ positiontab }}</v-list-item-title>
                                </v-list-item>
                            </v-list>
                        </v-menu>
                    </div>

                    <div class="text-center">
                        <v-menu offset-y>
                            <template v-slot:activator="{ on, attrs }">
                                <v-btn color="#AE78D6" dark v-bind="attrs" v-on="on" style="width: 140%;">
                                    แผนพัฒนาบุคลากร
                                </v-btn>
                            </template>
                        </v-menu>
                    </div>

                    <div class="text-center">
                        <v-menu offset-y>
                            <template v-slot:activator="{ on, attrs }">
                                <v-btn color="#AE78D6" dark v-bind="attrs" v-on="on">
                                    รายงานผลการดำเนินงาน
                                </v-btn>
                            </template>
                        </v-menu>
                    </div>
                </v-app-bar>
            </div>
        </div>
        <div class="Homepage">
            <v-btn depressed outlined plain raised>หน้าเเรก</v-btn>
        </div>
    </div>
</div>
</template>

<script>
import axios from 'axios';
import { end_point , out } from '../../config/config';
const url  = end_point + out
export default {
    data: () => {
        return ({
            // ContactTabinformation: {},
            information: ['ข้อมูลส่วนตัว', 'ข้อมูลบุคลากร', 'ข้อมูลอัตรากำลัง'],

            // ContactTabdevelopment: {},
            development: ['ข้อมูลการอบรม/สัมมนา/ดูงาน', 'ข้อมูลการใช้งบประมาณพัฒนาศักยภาพ', 'ข้อมูลการลาศึกษา', 'ข้อมูลบุคลากรดีเด่น'],

            // ContactTabposition: {},
            position: ['สถานะดำเนินการ', 'เอกสารประกอบการสอน / คำสอน', 'ผู้ดำรงตำแหน่งทางวิชาการ']
        })
    },
    computed: {
        informationState: {
            get() {
                // this.ContactTabinformation = this.$nuxt.$store.state.information
                return this.$nuxt.$store.state.information
            },
            set(val) {
                // console.log('information', this.$nuxt.$store.state.information)
                this.$store.commit('set_information', val)
                // console.log('information', this.$nuxt.$store.state.information)
            }
        },
        developmentState: {
            get() {
                // this.ContactTabdevelopment = this.$nuxt.$store.state.development
                return this.$nuxt.$store.state.development
            },
            set(val) {
                // console.log('development', this.$nuxt.$store.state.development)
                this.$store.commit('set_development', val)
                // console.log('development', this.$nuxt.$store.state.development)
            }
        },
        positionState: {
            get() {
                // this.ContactTabposition = this.$nuxt.$store.state.position
                return this.$nuxt.$store.state.position
            },
            set(val) {
                // console.log('position', this.$nuxt.$store.state.position)
                this.$store.commit('set_position', val)
                // console.log('position', this.$nuxt.$store.state.position)
            }
        }
    },
    methods: {
        async logout(){
            await fetch(url, {
              method: 'POST',
              headers: {'Content-Type': 'application/json'},
              credentials: 'include',
            });
            await this.$router.push('/auth/login')
        },
    },

};
</script>

<style>
@media only screen and (max-width: 1880px) {}
.test {
    border: 1px solid black;
    
    
}
.widtter {
    width: 100%;
    
}

.higther {
    height: 100%;
    
    /* height: auto; */
}   
  


/* .Hd {
  position: relative;
  top: -120px;
  left: -20px;
} */
/* .Img {
  width: 23%;
  position: relative;
  top: -50px;
  left: 5px;
} */

.Box {
    width: 70%;
    display: flex;
    
}


.v-toolbar__content,
.v-toolbar__extension {
    align-items: center;
    display: flex;
    justify-content: space-between;
    

}

.Homepage {
   position: relative;
    left: -1rem

}

</style>
