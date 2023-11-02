<script>
    import logo from "$lib/assets/icons/lamp-icon.svg";
</script>
<div class="caixa-formulario">
    <form action="" class="formu">
        <div class="icon-and-label">
            <img src={logo} alt="icone" class="icone">
            <label for="nome-completo">O que você precisa encontrar?</label>
        </div>
        <div class="input-container">
            <input name="nome-completo" placeholder="Digite o serviço desejado (ex: Eletricista, Encanador, Babá)..." type="email" required />
        </div>
    </form>
</div>
<div class="caixa-formulario2">
    <form action="" class="formu">
        <div class="icon-and-label">
            <img src={logo} alt="icone" class="icone">
            <label for="nome-completo">O que você precisa encontrar?</label>
        </div>
        <div class="input-container">
            <input name="nome-completo" placeholder="Digite o serviço desejado (ex: Eletricista, Encanador, Babá)..." type="email" required />
        </div>
    </form>
</div>

<style>
    .caixa-formulario {
        width: 710px;
        height: 87px;
        flex-direction: column;
        margin: 20px 20px 0px 20px;
        padding: 16px 75px 16px 24px ;
        align-items: center;
        border: 1.2px solid #CECECE;
        background: #FFF;

    }
    .caixa-formulario2 {
        width: 710px;
        height: 87px;
        flex-direction: column;
        margin: 0px 0px 20px 20px;
        padding: 16px 75px 16px 24px ;
        align-items: center;
        border: 1.2px solid #CECECE;
        background: #FFF;

    }
    .input-container {
        display: flex;
        flex-direction: column;
    }
    
    input{
        background-color: #ffffff;
        border: none;
        margin-left: 40px;
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
    }

    .icone {
        
    }

    .formu {
      
    }
</style>
