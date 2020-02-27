<template>
  <div id="information-tiler">
    <tile v-for="information in tileInformation" v-bind:key="information.title" v-bind:information="information"/>
  </div>
</template>

<script>
import Tile from "./Tile.vue";
export default {
  props: {
    tileInformation: Array // [{title, data}]
  },
  components: {
    Tile
  }
}
</script>

<style scoped>
#information-tiler {
  display: flex;
  flex-wrap: wrap; 
  justify-content: center;
  width: 100%;
  margin-top: 25px;
  margin-bottom: 25px;
}
</style>