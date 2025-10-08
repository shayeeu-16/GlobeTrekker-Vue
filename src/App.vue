<template>

  <div class="content">
    <Destination :title="item.title" :description="item.description" :image="item.image" v-for="item in destinations" />
  </div>
</template>
<script setup>
import Destination from './components/Destination.vue';
import Modal from './components/Modal.vue';
import Beach from './assets/beach.jpg'
import City from './assets/city.jpg'
import Mountain from './assets/mountain.jpg'
const destinations = [{
  title: 'Mountain',
  description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Corrupti perferendis, facilis mollitia commodi, odio doloremque ea ipsam ad sapiente ullam officia nostrum repellat maxime eveniet, voluptas delectus! Quo, impedit error.',
  image: Mountain
  
}, {
  title: 'Beach',
  description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Corrupti perferendis, facilis mollitia commodi, odio doloremque ea ipsam ad sapiente ullam officia nostrum repellat maxime eveniet, voluptas delectus! Quo, impedit error.',
  image: Beach
}, {
  title: 'City',
  description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Corrupti perferendis, facilis mollitia commodi, odio doloremque ea ipsam ad sapiente ullam officia nostrum repellat maxime eveniet, voluptas delectus! Quo, impedit error.',
  image: City
  
}, {
  title: 'Mountain',
  description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Corrupti perferendis, facilis mollitia commodi, odio doloremque ea ipsam ad sapiente ullam officia nostrum repellat maxime eveniet, voluptas delectus! Quo, impedit error.',
  image: Mountain
}, {
  title: 'Beach',
  description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Corrupti perferendis, facilis mollitia commodi, odio doloremque ea ipsam ad sapiente ullam officia nostrum repellat maxime eveniet, voluptas delectus! Quo, impedit error.',
  image: Beach
}, {
  title: 'City',
  description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Corrupti perferendis, facilis mollitia commodi, odio doloremque ea ipsam ad sapiente ullam officia nostrum repellat maxime eveniet, voluptas delectus! Quo, impedit error.',
  image: City
  
}]
</script>

<style scoped>
/* 
:root {
    --primary-color:#1E88E5; 
    --secondary-color: #F4511E;
    --neutral-color: #F5F5F5; 
    font-family: "Poppins", sans-serif;
    
} */
body{
  background-color: white;
}
.content{
    width: 100%;
    display: grid;
    grid-template-columns: 1fr 1fr 1fr; /* Creates three equal-width columns */
    gap: 20px;
    
}
</style>
