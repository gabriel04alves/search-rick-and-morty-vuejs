<template>
    <div class="footer" >
        <p class="text-footer">
            <img class="logo" src="../assets/images/github.svg" alt="github">
            <a class="text-footer" href="https://github.com/gabriel04alves">
                /gabriel04alves
            </a>
        </p>
        <p class="text-footer">
            <img class="logo" src="../assets/images/linkedin.svg" alt="linkedin">
            <a class="text-footer" href="https://linkedin.com/in/gabriel04alves">
                /gabriel04alves
            </a>
        </p>
    </div>
</template>

<style>
.footer {
    display: flex;
    justify-content: end;
    /* align-items: center; */
    flex-direction: row;
    position: fixed;
    gap: 1%;
    border-top: 0.25em solid;
    border-image: linear-gradient(60deg, #52b0cf, #97ce4c) 1 1;
    color: #F4F4F4; 
    height: 70px;
    width: 100%; 
    background-color: #002F40;
    padding: 1%;
}

.text-footer {
    font-family:'roboto', 'Times New Roman', Times, serif;;
    text-decoration: none;
    color: #f4f4f4;
    font-weight: 300;
    align-self: center;
    display: flex;
    justify-content: center;
    gap: 2.5px;
    font-size: 1.3vh;
}

.logo {
    height: 2.6vh;
    align-self: center;
}
@media (max-width: 1000px) {
    .footer {
        height: 50px;
        justify-content: center;
        gap: 15px;
    }
    .logo {
        height: 3vh;
    }
    .text-footer {
        margin-top: 0;
        align-self: center;
    }
}
</style>

<script>
export default {
	name: "my-component",
}
</script>