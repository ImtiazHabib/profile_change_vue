<script setup>
import {reactive} from 'vue';

const users = [
  {
    id:1,
    name:"imtiaz habib",
    description:"hello I am imtiaz habib and I love black",
    color:"black",
    img:"https://images.pexels.com/photos/936119/pexels-photo-936119.jpeg",
  },
   {
    id:1,
    name:"Arman Malik",
    description:"hello I am Arman Malik and I love red",
    color:"red",
    img:"https://images.pexels.com/photos/10392356/pexels-photo-10392356.jpeg",
  }
];


</script>

<template>
   <section class="container">
    <div class="row">
      <div class="col-md-12">
        <h1>Welcome to Profile change vue</h1>
      </div>
    </div>

   </section>
</template>

<style scoped>

</style>
