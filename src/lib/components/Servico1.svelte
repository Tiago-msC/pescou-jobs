<script>
// @ts-nocheck

import banner from '$lib/assets/foto-servico1.svg'
// @ts-ignore
export let Texto;
export let id;
</script>

<div class="corpo-servico" class:corpo-servico-impar={id % 2 === 1} >
    <div class="foto-nome">
        <div class="foto">
            <img src={banner} alt="Foto do prestador de serviço">
        </div>
        <div class="nome">
            <span>Serviço</span>
        </div>
    </div>
    <div class="id-preco-status">
        <span class="id">{id}</span>
        <span class="preco">R$ 60,00</span>
        <!-- svelte-ignore missing-declaration -->
        <div class="status" class:finalizado={Texto === 'Finalizado'} class:nao-finalizado={Texto !== 'Finalizado'}>

            {Texto}
        </div>
    </div>
</div>

<style>
    .nao-finalizado{
        background-color: #EE443A4D;
        color: #A12626;
    }
    .finalizado{
        background-color:  #8BCDFB4D;
        color: #268ABC;
    }
    .id-preco-status .id{
        margin-right: 70px;
    }
    .id-preco-status .preco{
        font-size: 1.125rem;
        font-style: normal;
        font-weight: 500;
        line-height: normal;
    }
    .id-preco-status .status{
        
        width: 151px;
        border-radius: 5px;
        padding: 10px 10px;
        font-weight: 500;
        text-align: center;
    }

    .id-preco-status{
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 102px;
    }
    .foto-nome img{
    height: 73px;
    width: 100px;
    background-color: aqua;
    border-radius: 5px;
    }
    .foto-nome{
    gap: 2.1875rem;
    display: flex;
    align-items: center;
    }
    .corpo-servico{
    display: flex;
    padding: 1.5rem 2.5rem;
    background: rgba(214, 214, 255, 0.50);
    align-items: center;
    justify-content: space-between;
    }
    .corpo-servico-impar{
    display: flex;
    padding: 1.5rem 2.5rem;
    background: var(--theme-color-white);
    align-items: center;
    justify-content: space-between;
    }


    @media screen and (max-width:64rem){
    .id-preco-status{
        gap: 1.25rem;
    }
    }
</style>