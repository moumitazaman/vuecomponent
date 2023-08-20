<script setup>
import { ref } from 'vue';
import ChildComponent from './ChildComponent.vue';
let message =ref("Message from Parent to Child !")

function updateMessage(childMessage) {
    message.value = childMessage
}
</script>

<template>
     <div class="mt-10 mb-10 bg-orange-600 p-10">
        <h1 class="text-black-900 text-xl my-5 ">Parent Component</h1>
        <ChildComponent :message="message" @messageEmitted="updateMessage"/>
        
    </div>
  
</template>

<style scoped>

</style>
