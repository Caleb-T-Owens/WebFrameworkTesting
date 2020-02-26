<template>

   <div id="header">
      <p id="name">Test Page</p>
      <div id="container-right">
         <header-links  v-for="link in links" v-bind:key="link.name" v-bind:link="link"/>
      </div>
   </div>
</template>

<script>
import HeaderLinks from "./HeaderLinks.vue";

export default {
   name: "Header",
   props: {
   },
   components: {
      HeaderLinks
   },
   data () {
      return {
         links: [
            {name: "Documentation", function: this.showDocumentation},
            {name: "Help", function: this.showHelp}
         ]
      }
   },
   methods: {
      showDocumentation() {
         
      },
      showHelp() {

      }
   }
}
</script>

<style scoped>
   #header {
      width: 100%;
      height: 40px;
      background-color: rgb(85, 85, 85);
      display: flex;
      align-items: center;
   }
   #name {
      color: white;
      font-size: 20px;
      padding-left: 5px;
   }

</style>