<script>
    import { RouterLink } from 'vue-router'
    export default {
        components: {
            RouterLink
        }
    }
</script>

<template>
    <div class="main">
        <div>

        </div>
        <nav>
            <RouterLink to="/">Home</RouterLink>
            <RouterLink to="/about">About</RouterLink>
          </nav>
    </div>
</template>

<style>
    .main {
        background-color: #002F40;
        width: 100%;
        height: 5rem;
    }
</style>