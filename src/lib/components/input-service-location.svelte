<script>
    import logo from "$lib/assets/icons/lamp-icon.svg";
    import pinlocalizacao from "$lib/assets/icons/pin-localizacao.svg";
</script>
<div class="caixa-formulario">
    <form action="" class="formu">
        <div class="icon-and-label">
            <img src={logo} alt="icone" class="icone">
            <label for="servico">O que você precisa encontrar?</label>
        </div>
        <div class="input-container">
            <input name="servico" placeholder="Digite o serviço desejado (ex: Eletricista, Encanador, Babá)..." type="text" required />
        </div>
    </form>
</div>
<div class="caixa-formulario">
    <form class="formu">
        <div class="icon-and-label">
            <img src={pinlocalizacao} alt="icone" class="icone">
            <label for="localizacao">Onde você precisa dos serviços?</label>
        </div>
        <div class="input-container">
            <input name="localizacao" placeholder="Informe a sua localização (ex: Bairro, Cidade, CEP)..." type="text" required />
        </div>
    </form>
</div>

<style>
    .caixa-formulario {
        width: 100%;
        flex-direction: column;
        /* margin: 20px 20px 0px 0px; */
        
        padding: 16px 75px 16px 24px ;
        align-items: center;
        border: 1.2px solid var(--theme-color-light-gray);
        border-collapse: collapse;
        background: var(--theme-color-white);
    }

    .icone {
        height: 24px;
    }
    
    .caixa-formulario + .caixa-formulario {
        border-collapse: collapse;
        margin-bottom: 20px;
    }
    .input-container {
        display: flex;
        flex-direction: column;
    }
    input{
        background-color: var(--theme-color-white);
        border: none;
        margin-left: 35px;
        width: 80%;
        outline: none;
    }


    .icon-and-label {
        font-weight: 600;
        display: flex;
        align-items: center;
        margin-bottom: 8px; 
    }

    label {
        margin-left: 11.8px;
        font-size: 0.9rem;
        color: var(--theme-color-secondary);
    }
</style>
