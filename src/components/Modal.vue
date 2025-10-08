<template>
        <!-- The Modal -->
    <div v-if="show" id="myModal" class="modal">
        <!-- Modal content -->
        <div class="modal-content">
            <h4>Booking Information</h4>
            <span class="close" @click="emits('close')" >&times;</span>
            <div class="content">
                <label>Destination: <span>{{ location }}</span></label>
                <div>
                    <label>Name: <input type="text" id="fullName" v-model="name"></label>
                </div>
            </div>
            <span id="name-error"></span>
            <button @click="submit">Submit</button>
        </div>

        <p>Hello Modal</p>
    </div>
</template>
<script setup>
    const { location, show } = defineProps(['location', 'show'])
    const emits  = defineEmits(['close'])
    console.log("location", location)
    console.log("show", show)

    function submit(){
        alert(`Thank you ${name.value}, your booking to ${location} is confirmed! `)
        emits('close')
    }
    
</script>
<style>
#myModal{ 

    position: fixed; /* Stay in place */
    z-index: 1; /* Sit on top */
    left: 0;
    top: 0;
    width: 100%; /* Full width */
    height: 100%; /* Full height */
    overflow: auto; /* Enable scroll if needed */
    background-color: rgb(0,0,0); /* Fallback color */
    background-color: rgba(0,0,0,0.4); /* Black w/ opacity */
    color: black;
}
.modal-content {
    background-color: #fefefe;
    margin: 15% auto; /* 15% from the top and centered */
    padding: 100px 20px;
    border: 1px solid #888;
    max-width: 500px;
    
}
.modal-content button{
    padding-top: 10px;
}
#myModal #name-error{
    color:red;;
    padding: 5px 0 ;
    font-size: 13px;
    font-style: italic;
    
}
/* The Close Button */
.close {
  color: #aaa;
  float: right;
  font-size: 28px;
  font-weight: bold;
}
</style>