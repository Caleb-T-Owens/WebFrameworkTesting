<template>
   <div id="header">
      <div id="name-container">
         <p id="name">Test Page</p>
      </div>
      <div id="container-right">
         <header-link class="link" v-for="link in links" v-bind:key="link.name" v-bind:link="link" />
      </div>
   </div>
</template>

<script>
   import HeaderLink from "./HeaderLink.vue";

   export default {
      name: "Header",
      props: {
         seen: Object
      },
      components: {
         HeaderLink
      },
      data() {
         return {
            links: [{
                  name: "Documentation",
                  function: this.showDocumentation
               },
               {
                  name: "Help",
                  function: this.showHelp
               }
            ]
         }
      },
      methods: {
         showDocumentation() {
            this.seen.isSeen = true;
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
      position: fixed;
      top: 0px;
   }
   #name-container {
      width: 150px;
   }
   #name {
      color: white;
      font-size: 20px;
      padding-left: 5px;
   }
   #container-right {
      width: calc(100% - 150px);
      display: flex;
      justify-content: flex-end;
   }
   .link {
      margin-right: 15px;
   }
</style>