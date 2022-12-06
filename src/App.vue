<template>
  <div class="container">
  <div class="header_txt">
  <Header_Rent titlename="RENTAL INFORMATION" propertytype="Commerical/Residential/Multi-Use"/>
  </div>
  <Rental_Box :property="property" />


</div>
</template>

<script>
import Header_Rent from './components/Header_Rent.vue'
import Rental_Box from './components/Rental_Box.vue'

export default {
  name: 'App',
  components: {
    Header_Rent,
    Rental_Box
  },

  data(){
    return {
      property : []
    }

  },

  methods: {

    // promises

      async fetchproperty(){
          const res = await fetch("https://vinuthna-rental.herokuapp.com/api")
          const data = await res.json()
          console.log(data)
          return data.property
      }


  },
  async created(){
    this.property = await this.fetchproperty()
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  /*color: #2c3e50;*/
  margin-top: 60px;
}
.header_txt {

  background-color:#F4A460;
}

.container {
  background-color: #FFFFFF;
}
</style>
