<script>
    let imagens = [
        { src: "vestido.png", alt: "Gótico" },
        { src: "short.png", alt: "Scene" },
        { src: "vestidolaranja.png", alt: "Scene" },
        { src: "cinto.png", alt: "Scene" }
    ];
</script>

<div class="header"> EXCENTRIKA WEAR</div>

<div class="content">
<div class="categories">
    <div><a href="/Gotico">Gótico</a></div>
    <div><a href="/Scene">Scene</a></div>
    <div><a href="/Boho">Boho</a></div>
</div>

    <div class="general">EXEMPLOS:</div>

    <div class="items">
        {#each imagens as imagem (imagem.src)}
            <div class="item">
                <img src={imagem.src} alt={imagem.alt} on:error={() => console.error("Erro ao carregar imagem:", imagem.src)} />
            </div>
        {/each}
    </div>
</div>

<style>
    * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }

    :global(body) {
        font-family: Arial, sans-serif;
        background-color: black;
        color: white;
    }

    .header {
        background-color: #7A1616;
        padding: 20px;
        font-size: 36px;
        font-weight: bold;
        text-transform: uppercase;
        text-align: center;
    }

    .content {
        background-color: black;
        min-height: 100vh; 
        padding: 20px;
    }

    .categories {
        display: flex;
        justify-content: center;
        gap: 20px;
        padding: 20px 0;
    }

    .categories div {
        background-color: gray;
        padding: 10px 20px;
        font-weight: bold;
        border-radius: 5px;
    }

    .categories a {
        text-decoration: none;
        color: black;
    }

    .general {
        font-size: 24px;
        text-align: left;
        margin-left: 10%;
        margin-top: 20px;
    }
    .items {
    display: flex;
    justify-content: center;
    flex-wrap: wrap; /* Permite que as imagens fiquem em várias linhas se necessário */
    gap: 20px;
    margin-top: 20px;
}

.item {
    padding: 0; /* Remove qualquer espaço extra ao redor da imagem */
    background: none; /* Remove o fundo branco */
    width: 200px; /* Define um tamanho fixo para as imagens */
    height: 250px; /* Ajusta a altura para manter uma proporção bonita */
    display: flex;
    align-items: center;
    justify-content: center;
}

.items img {
    width: 100%; /* Ajusta a imagem ao tamanho da div */
    height: 100%;
    object-fit: cover; /* Mantém a imagem bonita sem distorção */
    display: block;
    border-radius: 10px; /* Deixa as imagens com cantos arredondados para um visual bonito */
}
</style>
