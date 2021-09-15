<template>
  <div id="vue-hotel-list">    
    <HotelList/>
  </div>
</template>

<script>
import HotelList from './components/HotelList.vue'

export default {
  name: 'App',
  components: {
    HotelList
  }
}
</script>

<style>
#vue-hotel-list {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;  
}
</style>
