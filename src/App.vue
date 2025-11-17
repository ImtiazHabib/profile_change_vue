<script setup>
import { ref } from 'vue';

const users = [
  {
    id: 1,
    name: "imtiaz habib",
    description: "hello I am imtiaz habib and I love black",
    color: "black",
    img: "https://images.pexels.com/photos/936119/pexels-photo-936119.jpeg",
  },
  {
    id: 2,
    name: "Arman Malik",
    description: "hello I am Arman Malik and I love red",
    color: "red",
    img: "https://images.pexels.com/photos/10392356/pexels-photo-10392356.jpeg",
  }
];

// to track the user 
const currentUserIndex = ref(0);
const iterate = ()=>{
   currentUserIndex.value = (currentUserIndex.value + 1) % users.length; // Loop through users
}

</script>

<template>
  <section class="container">
    <div class="row">
      <div class="col-md-12">
        <h1>Welcome to Profile change vue</h1>
      </div>
    </div>

  </section>

  <section class="image_section">
    <div class="container">
      <div class="row">
        <div class="col-md-12">
          <div class="card" style="width: 18rem;">
            <img :src="users[currentUserIndex].img" class="card-img-top" alt="...">
            <div class="card-body">
               <h5 class="card-title">{{ users[currentUserIndex].name }}</h5>
              <p class="card-text">{{ users[currentUserIndex].description }}</p>
              <a href="#" class="btn btn-primary">Go somewhere</a>
            </div>
          </div>

          <!-- BUTTON TO CHANGE -->
           <button @click="iterate">
               change the post 
           </button>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped></style>
