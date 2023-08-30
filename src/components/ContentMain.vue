<template>
    <div class="all">
        <div class="title02"> 
            <img src="../assets/images/search.svg" alt="search" style="width: 3vh; align-self: center;"> 
            Buscar personagens
        </div>
        <form class="form" action="" method="get">
            <div class="search">
                <label class="textInput" for="searchId">ID do personagem: </label>
                <input class="inputId" name="searchId" type="number" id="characterId">
            </div>
            <div class="opitions">
                <div class="opition">
                    <label class="textInput" for="name">Nome</label>
                    <input class="checkbox" name="name" type="checkbox">
                </div>
                <div class="opition">
                    <label class="textInput" for="status">Status</label>
                    <input class="checkbox" name="status" type="checkbox">
                </div>
                <div class="opition">
                    <label class="textInput" for="specie">Espécie</label>
                    <input class="checkbox" name="specie" type="checkbox">
                </div>
                <div class="opition">
                    <label class="textInput" for="gender">Gênero</label>
                    <input class="checkbox" name="gender" type="checkbox">
                </div>
                <div class="opition">
                    <label class="textInput" for="origin">Planeta de origem</label>
                    <input class="checkbox" name="origin" type="checkbox">
                </div>                
            </div>
            <div class="btns">
                <button class="search-btn" id="btn-go">
                    Buscar
                </button>
                <button class="reset-btn" type="reset" id="btn-reset">
                    Limpar
                </button>
            </div>
        </form>
        <div id="result-style">
            <div id="results"></div>
            <img src="" alt="" id="img">
        </div>
    </div>
</template>

<script>
import '../assets/css/content.css'

document.addEventListener('DOMContentLoaded', () => {
    const characterId = document.getElementById('characterId');
    const btnGo = document.getElementById('btn-go');
    const results = document.getElementById('results');
    const image = document.getElementById('img')

    const fetchApi = (value) => {
        const result = fetch(`https://rickandmortyapi.com/api/character/${value}`)
        .then((res) => res.json())
        .then((data) => {
            console.log(data);
            return data;
        });
        return result;
    }

    btnGo.addEventListener('click', async (event) => {
        event.preventDefault();
        const result = await fetchApi(characterId.value);
        results.textContent = `${JSON.stringify(result, undefined, 2)}`;
        image.src = `${result.image}`
    });
});
</script>
