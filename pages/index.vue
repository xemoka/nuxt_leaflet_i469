<template>
  <div>
    <h1> Leaflet Version: {{ leafletVersion }} </h1>
  </div>
</template>

<script>
// import L from '~plugins/leaflet' // fails

export default {
  data () {
    return {
      leafletVersion: ''
    }
  },
  components: {
  },
  mounted () {
    const L = require('leaflet') // succeeds
    this.leafletVersion = L.version
  }
}
</script>

<style src="leaflet/dist/leaflet.css" lang="css"></style>
<style>
.container
{
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
.title
{
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}
.subtitle
{
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}
.links
{
  padding-top: 15px;
}
</style>
