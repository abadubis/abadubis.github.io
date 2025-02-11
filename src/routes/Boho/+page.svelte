<script>
    let vestidos = [
        {
            src: "calça.jpeg",
            descricao: "Tamanhos: PP a G , Plus Size de 1XL a 4XL",
            link: "https://br.shein.com/ROMWE-Fairycore-Boho-Style-Loose-Women-s-Wide-Leg-Pants-With-Star-Moon-And-Plant-Collage-Print-p-38364593.html?mallCode=1&imgRatio=3-4"
        },
        {
            src: "nãovoutrabalhar.png",
            descricao: "Tamanhos: PP a G",
            link: "https://br.shein.com/ROMWE-Hippie-Women-Bohemian-Flare-Sleeve-Paisley-Print-Blouse-p-45081329.html?imgRatio=&main_attr=27_81&mallCode=1" 
        },
        {
            src: "vestidolaranja.png",
            descricao: "Tamanhos: PP a G, Plus Size de 0XL a 4XL",
            link: "https://br.shein.com/SHEIN-MOD-Vintage-Floral-Print-Tie-Front-Bell-Long-Sleeves-Crop-Top-p-13463506.html?mallCode=1&imgRatio=3-4"
        },
        {
            src: "saia.jpeg",
            descricao: "Tamanhos: PP a G",
            link: "https://br.shein.com/ROMWE-PUNK-Patchwork-Print-Layered-Hem-Skirt-p-25829024.html?mallCode=1&imgRatio=3-4"
        }
    ];
</script>

<div class="header">BOHO</div>

<div class="container">
    <div class="vestidos">
        {#each vestidos as vestido}
            <div class="vestido">
                <img src={vestido.src} alt="Vestido Gótico" />
                <p>{vestido.descricao}</p>
                <a href={vestido.link} target="_blank">Ver Produto</a>
            </div>
        {/each}
    </div>

    <div class="footer">
        <a href="/" class="back-button">← Voltar para Página Inicial</a>
    </div>
</div>

<style>
    * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }

    .header {
        background-color: #7A1616;
        padding: 20px;
        font-size: 36px;
        font-weight: bold;
        text-transform: uppercase;
        text-align: center;
        color: white;
    }

    .container {
        background-color: black;
        padding: 20px;
        min-height: 100vh;
        text-align: center;
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    .vestidos {
        display: flex;
        justify-content: center;
        flex-wrap: wrap;
        gap: 20px;
        margin-bottom: 30px;
    }

    .vestido {
        background-color: white;
        padding: 15px;
        border-radius: 10px;
        text-align: center;
        width: 220px;
    }

    .vestido img {
        width: 100%;
        border-radius: 5px;
    }

    .vestido p {
        font-size: 14px;
        margin: 10px 0;
        color: black;
    }

    .vestido a {
        display: inline-block;
        margin-top: 10px;
        padding: 8px 12px;
        background-color: #7A1616;
        color: white;
        text-decoration: none;
        border-radius: 5px;
        font-weight: bold;
    }

    .vestido a:hover {
        background-color: #5a0f0f;
    }

    .footer {
        margin-top: 40px;
        text-align: center;
    }

    .back-button {
        display: inline-block;
        padding: 10px 15px;
        background-color: #7A1616;
        color: white;
        text-decoration: none;
        font-weight: bold;
        border-radius: 5px;
        transition: 0.3s;
    }

    .back-button:hover {
        background-color: #5a0f0f;
    }
</style>