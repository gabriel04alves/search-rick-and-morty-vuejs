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
                    <input class="checkbox" name="name" id="name" type="checkbox">
                </div>
                <div class="opition">
                    <label class="textInput" for="status">Status</label>
                    <input class="checkbox" name="status" id="status" type="checkbox">
                </div>
                <div class="opition">
                    <label class="textInput" for="species">Espécie</label>
                    <input class="checkbox" name="species" id="species" type="checkbox">
                </div>
                <div class="opition">
                    <label class="textInput" for="gender">Gênero</label>
                    <input class="checkbox" name="gender" id="gender" type="checkbox">
                </div>
                <div class="opition">
                    <label class="textInput" for="origin">Planeta de origem</label>
                    <input class="checkbox" name="origin" id="origin" type="checkbox">
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

    const keys = ['name', 'status', 'species', 'gender', 'origin'];

    const buildResult = (result) => {
        const newObject = {};
        keys.map((key) => document.getElementById(key))
            .map((elem) => {
                elem.checked && (newObject[elem.name] = result[elem.name]);
            });
        return newObject;
    }

    btnGo.addEventListener('click', async (event) => {
        event.preventDefault();
        const result = await fetchApi(characterId.value);
        // results.textContent = `${JSON.stringify(result, undefined, 2)}`;
        results.textContent = `${JSON.stringify(buildResult(result), undefined, 2)}`;
        console.log(buildResult(result))
        image.src = `${result.image}`
    });
});
</script>
