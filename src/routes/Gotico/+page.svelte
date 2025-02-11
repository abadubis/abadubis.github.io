<script>
    let vestidos = [
        {
            src: "vestido.png", alt: "Gótico" ,
            descricao: "Tamanhos: PP a GG",
            link: "https://br.shein.com/ROMWE-Goth-Women-Off-Shoulder-Front-Ruched-Cross-Pendant-Flare-Sleeve-Contrast-Lace-Velvet-Vintage-Dress-For-New-Year-p-43740249.html?mallCode=1&imgRatio=3-4"
        },
        {
            src: "vestido2.png",
            descricao: "Tamanhos: PP a G, Plus Size de 1XL a 4XL, Curve+ de 5XL a 8XL",
            link: "https://br.shein.com/SHEIN-MOD-Grommet-Lace-Up-Front-Puff-Sleeve-Dress-p-12677650.html?mallCode=1&imgRatio=3-4" 
        },
        {
            src: "vestido3.png",
            descricao: "Tamanhos: PP a G, Plus Size de 1XL a 4XL",
            link: "https://br.shein.com/ROMWE-Goth-Retro-Gothic-Style-Flocked-Cross-Floral-Mesh-Contrast-Lace-Up-Waist-Women-Dress-For-New-Year-p-39767941.html?mallCode=1&imgRatio=3-4"
        },
        {
            src: "vestido4.png",
            descricao: "Tamanhos: PP a GG",
            link: "https://br.shein.com/ROMWE-Goth-Gothic-Wedding-Ball-Dark-Lady-Mature-High-Slit-Lace-Asymmetrical-Hem-Stand-Collar-Bell-Sleeve-Cross-Chain-Hollow-Plunge-Dress-For-Women-p-47004660.html?mallCode=1&imgRatio=3-4"
        }
    ];
</script>

<div class="header">GÓTICO</div>

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
    justify-content: center; /* Centraliza os itens na linha */
    flex-wrap: wrap; /* Permite que os itens quebrem para a linha de baixo */
    gap: 20px; /* Espaço entre os vestidos */
    margin-bottom: 30px;
    max-width: 90%; /* Limita a largura para manter uma boa disposição */
}

.vestido {
    background: white;
    padding: 10px;
    border-radius: 10px;
    text-align: center;
    width: 180px; /* Define uma largura fixa */
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
    color: black;
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