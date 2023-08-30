<template>
<button :class="'btn ' + type" @click="onClick">
    <slot></slot> <!-- Permitir contenido personalizado -->
</button>
</template>

<script>
export default {
props: {
    type: {
    type: String,
    default: 'default' // p. ej., 'primary', 'secondary'
    }
},
methods: {
    onClick(event) {
    this.$emit('click', event); // Emitir evento click para que los padres puedan escucharlo
    }
}
};
</script>
    