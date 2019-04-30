<template>
  <div id="app">
    <p>{{color}}</p>
    <ColorPanel :color=color />
    <DrawPanel/>
  </div>
</template>

<script>
import Pixel from './components/Pixel'
import DrawPanel from './components/DrawPanel'
import ColorPanel from './components/ColorPanel'

export default {
  name: "app",
  components: {
    DrawPanel,
    ColorPanel,
    Pixel
  },
  data: function(){
    return {
      color: 'white'
    }
  },
  mounted() {
    this.$root.$on('updatecolor', color => {
      this.color = color
    })
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
