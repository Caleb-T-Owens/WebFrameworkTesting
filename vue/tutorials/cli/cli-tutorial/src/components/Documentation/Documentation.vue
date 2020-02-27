<template>
  <div id="container">
     <div id="main">
        <div id="close-container">
           <p v-on:click="closeDocumentation()" id="close-button">Close</p>
        </div>
        <div id="main-container">
        </div>
     </div>
  </div>
</template>

<script>
export default {
   name: "Documentation",
   props: {
      seen: Object
   },
   methods: {
      closeDocumentation () {
         this.seen.isSeen = false;
      }
   }
}
</script>

<style scoped>
   #container {
      position: absolute;
      width: 100%;
      height: 100%;
      background-color: rgba(0, 0, 0, 0.205);
   }
   #main {
      margin-top: 50px;
      margin-left: 50px;
      width: calc(100% - 100px);
      height: calc(100% - 100px); 
      background-color: white;
   }
   #close-container {
      float:right
   }
   #close-button {
      margin-top: 5px;
      margin-right: 5px;
   }
</style>