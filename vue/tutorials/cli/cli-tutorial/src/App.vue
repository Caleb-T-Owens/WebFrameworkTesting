<template>
   <div id="app">
      <documentation v-if="seen"/>
      <Header/>
   </div>
</template>

<script>
   import Header from "./components/Header.vue";
   import Documentation from "./components/Documentation.vue";

   export default {
      name: 'App',
      components: {
         Header,
         Documentation
      }
   }
</script>

<style>
   * {
      margin: 0px;
      padding: 0px;
      font-family: 'Roboto Mono';
   }

   #app {}
</style>