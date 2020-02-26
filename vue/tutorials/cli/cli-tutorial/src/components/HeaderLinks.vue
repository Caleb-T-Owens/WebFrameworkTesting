<template>
   <p v-on:click="link.function()">{{link.name}}</p>
</template>

<script>
export default {
   name: "HeaderLinks",
   props: {
      link: Object
   }
}
</script>

<style>

</style>