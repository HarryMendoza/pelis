<template>
<div class="avatar-container">
    <img :src="imageUrl" alt="Avatar" class="avatar-image" />
</div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
name: 'Avatar',
props: {
    imageUrl: {
    type: String,
    required: true
    }
}
});
</script>

<style scoped>
.avatar-container {
    width: 40px; 
    height: 40px;
    overflow: hidden;
    border-radius: 50%; 
    display: flex;
    justify-content: center;
    align-items: center;
}

.avatar-image {
    width: 100%;
    height: 100%;
    object-fit: cover;
}
</style>
  