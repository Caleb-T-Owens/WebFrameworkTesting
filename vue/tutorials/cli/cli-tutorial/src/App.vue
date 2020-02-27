<template>
   <div id="app">
      <documentation v-bind:seen="seen" v-if="seen.isSeen"/>
      <Header id="header" v-bind:seen="seen"/>
      <Main id="main-container"/>
   </div>
</template>

<script>
   import Header from "./components/Header.vue";
   import Documentation from "./components/Documentation/Documentation.vue";
   import Main from "./components/Main/Main.vue"

   export default {
      name: 'App',
      components: {
         Header,
         Documentation,
         Main
      },
      data () {
         return {
            seen: {
               isSeen: false
            }
         }
      }
   }
</script>

<style>
   * {
      margin: 0px;
      padding: 0px;
      font-family: 'Roboto Mono';
   }
   #main-container {
   width: calc(100% - 100px);
    height: calc(100% - 80px);
    max-height: calc(100% - 80px);
    overflow: auto;
}
</style>

<style scoped>

</style>