<script setup>
import Navbar from './components/Navbar.vue';
import { Cropper } from 'vue-advanced-cropper'
import 'vue-advanced-cropper/dist/style.css';
import { ref } from "vue"
const img = "https://images.unsplash.com/photo-1534596292079-6ab51b3b0507?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=987&q=80"

const resized = ref(false)


</script>

<template>
<Navbar />
<Cropper v-if="!resized" class="cropper" :src="img" :stencil-props="{aspectRatio:1/1}" resizeImage="true">
</Cropper>
<button class="button" @click="">Resize</button>
</template>

<style scoped>

</style>
