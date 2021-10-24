<template>
    <v-app>
      <div>
        <Core-Nav/>
        <Nuxt/>
        <Core-Footer/>
        <div>
          <p v-if="!auth">ยังไม่ login</p>
          <p v-if="auth">login ละ</p>
        </div>

      </div>
    </v-app>

</template>

<script>
export default {
  name: 'layout',
  data() {
    return {
      auth: false
    }
  },
  mounted() {
    this.$nuxt.$on('auth', auth => {
      this.auth = auth;
    })
  },
}
</script>

<style>
::-webkit-scrollbar {
  display: none;
}
 
/* #app{
  margin: 0;
  padding: 0;
}

.Nav{
  height: 15%;
} */
</style>