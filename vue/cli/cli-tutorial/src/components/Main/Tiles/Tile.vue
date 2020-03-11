<template>
  <div id="information-container">
     <h2>{{information.title}}</h2>
     <p>{{information.data}}</p>
  </div>
</template>

<script>
export default {
   props: {
      information: Object // {title, data} 
   }
}
</script>

<style scoped>
#information-container {
   width: 300px;
   min-width: 300px;
   margin: 25px;
}
</style>