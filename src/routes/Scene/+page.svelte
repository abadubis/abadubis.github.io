<script>
    let vestidos = [
        {
            src: "short.png",
            descricao: "Tamanhos: PP a G",
            link: "https://br.shein.com/ROMWE-J-Fashion-Y2K-Gyaru-Himekaji-Low-Waist-Vintage-Zebra-Furry-Patchwork-Star-Rhinestone-Decor-Denim-Shorts-p-49377781.html?mallCode=1&imgRatio=3-4"
        },
        {
            src: "cinto.png",
            descricao: "Tamanhos: 105 a 125 centímetros",
            link: "https://br.shein.com/1pc-Unisex-Punk-Style-Rivet-Pyramid-Studded-PU-Belt-Accessory-Suitable-For-Daily-Wear-Great-Gift-For-Boyfriend-Girlfriend-On-Valentine-s-Day-p-44985308.html?mallCode=1&imgRatio=3-4" 
        },
        {
            src: "short2.jpeg",
            descricao: "Tamanhos: PP a GG, Plus Size de 1XL a 4XL",
            link: "https://br.shein.com/ROMWE-Grunge-Punk-Gyaru-Punk-Style-Skull-Head-Embroidery-Tight-Sexy-Ultra-Short-Denim-Hot-Pants-With-Back-Pocket-School-p-33928825.html?mallCode=1&imgRatio=3-4"
        },
        {
            src: "blusa.jpeg",
            descricao: "Tamanhos: PP a GG",
            link: "https://br.shein.com/Attitoon-Pink-Contrast-Checkerboard-Print-Women-s-Casual-Sexy-Camisole-Tank-Top-Suitable-For-Summer-p-38120380.html?mallCode=1&imgRatio=3-4"
        }
    ];
</script>

<div class="header">SCENE</div>

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
    justify-content: center; /* Centraliza os itens horizontalmente */
    flex-wrap: wrap; /* Permite quebra de linha em telas menores */
    gap: 20px; /* Espaço entre os itens */
    margin-bottom: 30px;
    max-width: 90%;
}

.vestido {
    background: white; /* Fundo branco para destaque */
    padding: 10px;
    border-radius: 10px;
    text-align: center;
    width: 180px; /* Tamanho compacto e organizado */
    box-shadow: 0 4px 8px rgba(255, 255, 255, 0.2);
}

.vestido img {
    width: 100%;
    height: auto;
    object-fit: cover;
    display: block;
    border-radius: 10px 10px 0 0;
}

.vestido p {
    font-size: 12px;
    margin: 5px 0;
    color: black; /* Texto escuro para contraste */
    background: white;
    padding: 5px;
    border-radius: 0 0 10px 10px;
}

.vestido a {
    display: inline-block;
    margin-top: 5px;
    padding: 6px 10px;
    background-color: #7A1616;
    color: white;
    text-decoration: none;
    border-radius: 5px;
    font-weight: bold;
    font-size: 12px;
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