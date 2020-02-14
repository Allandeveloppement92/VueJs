<template>
  <div>
    <h1 style="margin-top:30px; margin-bottom:15px;">Nos films</h1>

    <div v-for="film in info" :key="film.imbID" style="font-size:20px; margin-top:10px;">



          
               {{film.Title}}
            {{film.Year}}
            <img :src="film.Poster" alt="imgLoaded"/>
          

          
          
    </div>
  </div>
</template>

<script>
//import Test from'./../components/Test.vue'
const axios = require('axios').default;

export default {
  name: 'HomePage',
  components: {
    // Test
  },
  props: {
    message: String
  },
 data() {
    return {
            info:[],
            };
        },
  
  mounted() {
    axios
      .get('http://www.omdbapi.com/?s=batman&apikey=904eed5c')
      .then(response => (this.info = response.data.Search))
  }
}
</script>

<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>