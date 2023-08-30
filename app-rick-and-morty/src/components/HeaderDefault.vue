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
        <h1 class="title"> 
            <img src="../assets/images/logo.svg" alt="rick" class="img-rick">
            <p><RouterLink class="router-link" active-class="active" to="/">Search Rick And morty</RouterLink></p> 
        </h1>
        <h2 class="btn">
            <RouterLink class="router-link" active-class="active" to="/about">About</RouterLink>
        </h2>
    </div>
</template>

<style>
    .main {
        background-color: #002F40;
        height: 100px;
        width: 100%;
        display: flex;
        justify-content: space-between;
        align-items: center;
        flex-direction: row;
        font-family: 'Raleway', 'Times New Roman', Times, serif;
        padding: 20px;
        border-bottom: 0.25em solid;
        border-image: linear-gradient(60deg, #97ce4c, #52b0cf) 1 1;
    }
    .title, .btn {
        font-family: 'phudu', 'Times New Roman', Times, serif;
        display: flex;
        align-items: center;
        font-weight: 400;
        font-size: 2vh;
        color: #F7F7F7;
        display: flex;
        text-align: center;
        vertical-align: middle;
        flex-direction: row;
        gap: 5px;
    }
    .router-link {
        color: #f7f7f7d0;
        font-weight: 300;
        font-size: 2vh;
        text-decoration: none;
    }
    
    .active {
        font-weight: 600;
        text-shadow: 1px #000;
    }
    .img-rick {
        width: 5vh;
    }
    @media (max-width: 400px) {
        .main {
            height: 90px;
        }
    }
</style>