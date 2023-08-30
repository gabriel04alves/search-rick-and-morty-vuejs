<template>
    <div class="all">
        <div class="title02"> 
            <img src="../assets/images/search.svg" alt="search" style="width: 3vh; align-self: center;"> 
            Buscar personagens
        </div>
        <form class="form" action="">
            <div class="search">
                <label class="textInput" for="searchId">ID do personagem: </label>
                <input class="inputId" name="searchId" type="number">
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
                <button class="search-btn" type="submit" id="btn-go">
                    Buscar
                </button>
                <button class="reset-btn" type="reset" id="btn-reset">
                    Limpar
                </button>
            </div>
        </form>
    </div>
</template>

<style>
.all {
    display: flex;
    flex-direction: column;
    /* justify-content: center; */
    align-items: center;
    height: 50rem;
}
.title02, .textInput, .inputId {
    color: #002F40;
}
.textInput, .inputId {
    font-weight: 350;
}
.title02 {
    font-family: 'Roboto', 'Times New Roman', Times, serif;
    margin-top: 5%;
    text-transform: uppercase;
    font-weight: 400;
    font-size: 3vh;
    display: flex;
    justify-content: center;
    margin-bottom: 1%;
}
.form {
    display: flex;
    align-items: center;
    flex-direction: column;
}
.textInput {
    font-family: 'Roboto', 'Times New Roman', Times, serif;
    font-size: 1.8vh;
}
.opitions {
    display: flex;
    gap: 0.5em;
    margin-top: 0.25em;
    
}
.opition {
    display: flex;
    gap: 0.15em;
}
.checkbox, .inputId {
    max-height: 3vh;
    border: solid 1px;
    border-radius: 5px;
}

.checkbox {
    cursor: pointer;
    border: 3px solid #97ce4c;
    border-radius: 10px;
}
.inputId {
    padding: 3px;
    font-family: 'Roboto', 'Times New Roman', Times, serif;   
}
.btns {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 10px;
    margin-top: 3%;
}

.search-btn, .reset-btn {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 10vh;
    height: 3vh;
    border-radius: 10px;
    font-family: 'phudu','Times New Roman', Times, serif;
    font-size: 1.6vh;
    cursor: pointer;
    
}
.search-btn:hover, .reset-btn:hover  {
    transform: translateY(-8px);
}
.search-btn:active, .reset-btn:active  {
    transform: scale(0.90);
}


.search-btn {
    background-color: #FFF;
    border: solid 0.3vh #97ce4c;
    color: #97ce4c;
}
.reset-btn {
    background-color: #FFF;
    border: solid 0.3vh #c7321d;
    color: #c7321d;
}


@media (min-width: 100px) and (max-width: 950px) {
    .all {
        margin: 0px 10px 0px 10px;
    }
    .opition {
        display: flex;
        align-items: center;
        gap: 0.10em;
    }
    .textInput {
        font-size: 1.5vh;
    }
}
</style>

<script>

</script>