<div class="input">
    <form action="" class = "formu">
        <img src="" alt="icone" class="icone">
        <label for="nome-completo">Nome completo</label>
        <div class="input-container">
            <input name="nome-completo" placeholder="Insira seu nome completo"type="email" required />
        </div>
    </form>
</div>

<style>
    .input {
    display: flex;
    margin: 20px;
    padding: 20px;
    align-items: center; /* Mudamos o alinhamento vertical para o centro */
    border: 1.2px solid #CECECE;
    background: #FFF;
}

.icone {
    margin-right: 10px; /* Adicionamos uma margem direita para separar os elementos */
}

.formu {
    /* Removemos o display flex e o justify-content, pois eles não são necessários */
}

</style>