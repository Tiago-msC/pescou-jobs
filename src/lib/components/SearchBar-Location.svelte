<script>
    import '../../styles.css';
    import pinlocation from '$lib/assets/icons/pin-localizacao-outline.svg';
</script>




<div class="caixa-formulario">
    <form action="" class="formu">
        <div class="icon-and-label">
            <img src={pinlocation} alt="icone" class="icone">
        </div>
        <div class="input-container">
            <input name="localizacao" placeholder="Imbiribeira, Recife, Pernambuco" type="text" />
        </div>
    </form>
</div>
<style>
    input{
        background-color: var(--theme-color-white);
        border: none;
        outline: none;
        align-items: center;
        width: 280px;
    }
    .icon-and-label{
        margin-top: 3px;
        width: 25px;
        height: 25px;
    }
    .input-container{
        width: 339px;
        align-self: stretch;
        color: var(--theme-text-color-secondary);
        outline: none;
        border: none;
    }
    .formu{
        display: flex;
        align-items: center;
        gap: 8px;
    }
    .caixa-formulario{
        display: flex;
        width: 339px;
        padding: 16px 24px;
        gap: 9px;
        border: 1px solid var(--theme-color-light-gray);
        background: var(--theme-color-white);
    }
</style>