<script>
    import logo from "$lib/assets/icons/lamp-icon.svg";
</script>
<div class="input">
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
    .input {
        display: flex;
        /* flex-direction: column; */
        margin: 20px;
        padding: 20px;
        align-items: center;
        border: 1.2px solid #CECECE;
        background: #FFF;
    }

    .icon-and-label {
        display: flex;
        align-items: center;
        margin-bottom: 10px; 
    }

    label {
        margin-left: 10px; 
    }

    .icone {
        margin-right: 10px;
    }

    .formu {
       
    }
</style>
