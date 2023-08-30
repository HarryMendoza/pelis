<template>
<div class="card">
    <img v-if="image" :src="image" alt="Card Image" class="card-image"/>
        <div class="card-content">
            <h2 class="card-title">{{ title }}</h2>
            <p class="card-description">{{ description }}</p>
    <slot></slot> 
    </div>
</div>
</template>

<script>
export default {
props: {
    image: {
    type: String,
    default: null
    },
    title: {
    type: String,
    default: ''
    },
    description: {
    type: String,
    default: ''
    }
}
};
</script>
