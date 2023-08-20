<script setup>
defineProps(['message'])
defineEmits(['messageEmitted'])

</script>

<template>
    <div class="mt-10 mb-10 bg-orange-300 p-4">
        <h1 class="text-black-900 text-xl my-5">Child Component</h1>
        <h4 class="text-white-900">{{ message }}</h4>

        <button @click="$emit('messageEmitted', 'Message from Child to Parent')" class="bg-blue-500 hover:bg-blue-700 text-white font-bold my-8 py-2 px-4 rounded">
            Button
        </button>
    </div>
  
</template>

<style scoped>

</style>
