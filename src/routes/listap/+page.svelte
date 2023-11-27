<script>
    import HeaderSearcher from "$lib/components/Header-Searcher.svelte";
    import arrow_right from "$lib/assets/icons/slight-arrow-right.svg";
    import ServiceCategories from "$lib/components/ServiceCategories.svelte";
    import '../../styles.css';
    import star_active from "$lib/assets/icons/star-avaliation.svg";
    import imagem_perfil from '$lib/assets/image-perfil.svg';
    import verified from '$lib/assets/icons/verified.svg';
    import pin_localizacao from '$lib/assets/icons/pin-localizacao.svg'
    import foto_perfil_grande from '$lib/assets/icons/foto-perfil-grande.svg'
    import Button from "$lib/components/Button.svelte";

    const handleNavigateProfessionals = () => {
    window.location.href = "/profissionais";
  };
</script>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Perfil</title>

<HeaderSearcher></HeaderSearcher>
<ServiceCategories/>


<body>
    
    <div class="head-nav">
        <div class="navbar">
            <span class="inicio">Início</span>
            <img src={arrow_right} alt="Seta p/ direita">
            <span>Eletricistas</span>
            <img src={arrow_right} alt="Seta p/ direita">
            <span>Eletricista1002</span>
        </div>
        <div class="profissional-procurado">
            <span class="texto-profissional">Seu eletricista de confiança para iluminar e proteger.</span>
            <div class="avaliacao">
                <img src={star_active} alt="Estrela">
                <span class="numero-avaliacao" style="font-weight: 600;">4.5 <b style="font-weight: 400;color:#777">(<b style="font-weight: 400; text-decoration-line:underline">5</b>)</b></span>
            </div>
        </div>
        
    </div>
    
    <div class="container-foto-nome">
        <img src={foto_perfil_grande} alt="Foto de perfil">
        <div class="nome-localizacao-botao">
            <div class="foto-nome-verified">
                <span class="nome-prestador">Marcos Antônio</span>
                <img src={verified} alt="Verificado">
            </div>
            <div class="localizacao">
                <img src={pin_localizacao} alt="">
                <div class="localizacao-texto">Imbiribeira, Recife, Pernambuco</div>
            </div>
            <div class="botao-contato">
                <Button
                    expended
                    text="Entre em contato comigo"
                    type="outline"
                    onClick={handleNavigateProfessionals}
                    />
            </div>
        </div>
    </div>

    <div class="titulo"><span id="titulo">Eletricista Profissional</span></div>
    <div class="corpo-descricao">
        <div class="descricao-texto">Lorem ipsum dolor sit amet consectetur adipisicing elit. Modi quibusdam provident illum aut enim praesentium, aspernatur iste cum! Dolorem sunt labore incidunt cumque voluptatibus sapiente vitae, sequi deleniti accusantium quisquam.  Lorem ipsum dolor sit amet consectetur adipisicing elit. Ratione libero, error beatae minima voluptatem, nemo deserunt porro odio iusto consequuntur pariatur id officia natus rem maxime numquam officiis corrupti aut? Lorem, ipsum dolor sit amet consectetur adipisicing elit. Dolor temporibus accusantium omnis, aut nemo alias iste blanditiis sint maiores fugiat laudantium odit saepe ratione quibusdam ad illum quia consectetur at! Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime, dicta, esse voluptatum dolores, minus enim reprehenderit non voluptatem tenetur at molestias iure! Expedita pariatur itaque nulla, unde inventore fuga in.</div>
    </div>
    <div class="tags-relacionadas">
        <div class="tag"><span id="tag_texto">Instalação elétrica residencial</span></div>
        <div class="tag"><span id="tag_texto">Reparo de circuitos elétricos</span></div>
    </div>
    


    <!-- Barra avaliacao -->
    <div class="container">
        <div class="barra star-progress-bar">
            <div class="vazio">
                <span class="progresso star-progress-shape" style="width:91.12959054453356%"></span>
            </div>
        </div>
    </div>
</body>
    
<style>
    
    .corpo-descricao{
        display: grid;
        border: 1px solid palegreen;
        width: 50%;
        gap:  30px;
    }
    .tag{
        color: var(--theme-color-text-primary);
        border-radius: 10vmin;
        background: #EEE;
        display: flex;
        padding: 10px 16px;
        align-items: center;
        gap: 10px;
    }
    .tags-relacionadas{
        display: flex;
        gap: 10px;
        padding: 20px 0px;
        border: #e4e5e7 1px solid;
    }
    .titulo{
        font-weight: 600;
        font-size: 2rem;
        padding: 10px 0px;
    }
    .localizacao{
        display: flex;
        align-items: center;
        gap: 10px;
        border: #e4e5e7 1px solid;

    }
    .nome-localizacao-botao{
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        gap: 8px;
        border: #e4e5e7 1px solid;

    }
    .foto-nome-verified{
        display: flex;
        align-items: center;
        gap: 10px;
        font-size: 1.5rem;
        font-weight: 600;
        border: #e4e5e7 1px solid;

    }
    .container-foto-nome > img{
        width: 20vmin;
        border-radius: 50%;
        border: #e4e5e7 1px solid;
    }
    .container-foto-nome{
        display: flex;
        align-items: center;
        width: 50%;
        justify-content: center;
        width: fit-content;
        gap: 18px;
        padding: 30px 0px;
        border: #4c7ee2 1px solid;
    }
    body{
        padding: 20px 120px ;
        background: #131313;
        display: flex;
        flex-direction: column;
    }
    .avaliacao{
        display: flex;
        align-items: center;
        top: 0;
        gap: 10px;
        border: #e4e5e7 1px solid;

    }
    .texto-profissional{
        font-size:2rem;
        font-weight: 600;
    }
    .profissional-procurado{
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        gap: 10px;
        width: 60%;

        border: #1dbf73 1px solid;
    }
    .navbar{
        display: flex;
        padding: 16px 0px;
        align-items: center;
        gap: 15px;
    }
    .head-nav{
        display: flex;
        width: auto;
        /* padding: 0px 134px; */
        flex-direction: column;
        align-items: flex-start;
        gap:23px;

    }
    .container {
        -webkit-box-direction: normal;
        border-collapse: collapse;
        border-spacing: 0;
        text-indent: 0;
        /* display: table-cell; */
        margin: auto;
        padding: 10px 10px 0 6px;

        vertical-align: top;
    }
    .barra .progresso {
        background: #1dbf73;
        border-radius: 999px;
        height: 100%;
        left: 0;
        position: absolute;
        z-index: 1;
    }
    .barra .vazio {
    -webkit-box-flex: 1;
    -ms-flex-positive: 1;
    background: #e4e5e7;
    border-radius: 999px;
    -webkit-flex-grow: 1;
    flex-grow: 1;
    height: 8px;
    position: relative;
}
    .barra {
    -webkit-box-align: center;
    -ms-flex-align: center;
    -webkit-align-items: center;
    align-items: center;
    display: -webkit-box;
    display: -webkit-flex;
    display: -ms-flexbox;
    display: flex;
    display: -webkit-box;
}
@media (max-width: 1024px){
    .profissional-procurado{
        width: 100%;
        padding: 20px;
    }
    body{
        padding: 30px 30px ;
    }
    .container {
        width: 100%;
        max-width: 720px;
    }
    .nome-localizacao-botao {

        padding: 10px;
    }

@media screen and (max-width: 768px) {
    .container-foto-nome{
        display: flex;
        flex-direction: column;
        width: 100%;
    }
    .nome-localizacao-botao .localizacao{
        padding: 10px;
    }
    .nome-localizacao-botao .localizacao, .nome-localizacao-botao .foto-nome-verified, .nome-localizacao-botao .botao-contato{
        width: 100%;
        justify-content: center;
    }
    .nome-localizacao-botao{
        display: flex;
        flex-direction: column;
        width: 100%;
    }
    .titulo{
        font-size: 1.5rem;
        justify-content: center;
        align-items: center;
        text-align: center;
        padding: 10px;

    }
    .corpo-descricao{
        border-radius: 5px;
        padding: 10px;
        width: 100%;
        height: 200px;
        overflow-y: auto;
    }
    .corpo-descricao .descricao-texto{
        font-size: 1rem;
        position: static;
    }
    .tag{
        font-size: 0.8rem;
    }
    .tags-relacionadas{
        position: relative;
        text-align: center;
        flex-direction: row;
        gap: 10px;
        justify-content: center;
        align-items: center;

    }
}
}

</style>