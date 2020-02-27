<template>
   <div id="main-container">
      <h1>Welcome to Test Page</h1>
      <h3>Easy to make test pages for programmers to learn from</h3>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Explicabo facere ratione eveniet est pariatur velit
         quos
         placeat quo omnis vel officia eos aperiam natus consequatur nobis, ad ipsa asperiores reiciendis?</p>
      <information-tiler v-bind:tileInformation="sellingPoints" />
   </div>
</template>

<script>
   import InformationTiler from "./Tiles/InformationTiler.vue";
   export default {
      name: "Main",
      components: {
         InformationTiler
      },
      data() {
         return {
            sellingPoints: [{
                  title: "Reason 1",
                  data: "orem ipsum dolor sit amet consectetur adipisicing elit. Explicabo facere ratione eveniet est pariatur velit quos placeat quo omnis vel officia eos aperiam natus consequatur nobis, ad ipsa asperiores reiciendis?"
               },
               {
                  title: "Reason 2",
                  data: "orem ipsum dolor sit amet consectetur adipisicing elit. Explicabo facere ratione eveniet est pariatur velit quos placeat quo omnis vel officia eos aperiam natus consequatur nobis, ad ipsa asperiores reiciendis?"
               },
               {
                  title: "Reason 3",
                  data: "orem ipsum dolor sit amet consectetur adipisicing elit. Explicabo facere ratione eveniet est pariatur velit quos placeat quo omnis vel officia eos aperiam natus consequatur nobis, ad ipsa asperiores reiciendis?"
               }
            ]
         }
      }
   }
</script>

<style scoped>
   #main-container {
      padding-left: 50px;
      padding-right: 50px;
      padding-top: 40px;
   }

   p {
      margin-right: 300px;
      margin-top: 3px
   }

   h3 {
      margin-top: -6px;
      color: gray;
   }
</style>