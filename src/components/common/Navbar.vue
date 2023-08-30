<template>
    <nav class="navbar">
        <ul>
            <li v-for="item in menuItems" :key="item.label">
                <router-link :to="item.path">{{ item.label }}</router-link>
            </li>
        </ul>
    </nav>
</template>

<script>
export default {
data() {
    return {
    menuItems: [
        { label: 'MOVIES', path: '/' },
        { label: 'CELEBS & PHOTOS', path: '/ruta2' },
        { label: 'COMUNITY', path: '/ruta3' },
        { label: 'NEWS', path: '/ruta4' }
    ]
    }
}
}
</script>
  
<style scoped>
.navbar {
    background-color: #333;
    padding: 10px 0;
}

.navbar ul {
    list-style-type: none;
    padding: 0;
    margin: 0;
    display: flex;
    justify-content: center;
}

.navbar li {
    margin: 0 15px;
}

.navbar a {
    text-decoration: none;
    color: white;
    padding: 5px 10px;
    transition: background-color 0.3s;
}

.navbar a:hover {
    background-color: yellow;
    color: #333;
}

</style>
