<template>
  <div class="home">
    <Main msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
// @ is an alias to /src
import Main from '@/components/Main.vue'

export default {
  name: 'Home',
  components: {
    Main
  },
  methods: {

  },
  created(){
    this.$axios.post("http://34.88.47.51/api/enter/main",{},{
      crossdomain: true,
      headers: {
        'accept-language': 11111998
      }
    }).then(res=>{
      console.log(res)
    })
  }
}
</script>
