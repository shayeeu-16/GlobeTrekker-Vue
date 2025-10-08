<template>
    <div class="places">
        <div class="destination">
            <img :src="image" :alt="title" width="100px" />
            <h3>{{ title }}</h3>
            <p>{{ description }}</p>
            <button id="bookBtn" @click="book(title)" type="submit">Book Now</button>
        </div>
        <Modal :show="isShow" :location="currentLocation" @close="()=> isShow=false" />
        
    </div>
</template>
<script setup>
import {ref} from 'vue'
import Modal from './Modal.vue'
const { image, title, description } = defineProps(['image', 'title', 'description'])
const isShow = ref(false)
const currentLocation = ref('')
function book(location) {
    currentLocation.value = location
    isShow.value = true
    
}

</script>

<style>
:root {
    --primary-color:#1E88E5; 
    --secondary-color: #F4511E;
    --neutral-color: #F5F5F5; 
    font-family: "Poppins", sans-serif;

}

.destination{
  width:300px;
  /* height: 400px; */
  background-color: var(--neutral-color);
  /* color: var(--primary-color); */
  padding: 10px 20px;
  
}
.destination h3{
    color: var(--primary-color);
}
.destination img{
    height: 200px;
    width: 100%;
}
button{
    background-color: var(--secondary-color);
    color: var(--neutral-color);
}
</style>
