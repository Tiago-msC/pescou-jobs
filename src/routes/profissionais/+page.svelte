<script>
    import '../../styles.css';
    import Card from '$lib/components/Card.svelte'
    import Header from '$lib/components/Header.svelte'
    import arrow_right from '$lib/assets/icons/slight-arrow-right.svg'
    import DropdownMenu from '$lib/components/Dropdown-menu.svelte';

    const cards = [
    { id: 1, title: 'Card 1' },
    { id: 2, title: 'Card 2' },
    { id: 3, title: 'Card 3' },
    { id: 4, title: 'Card 4' },
  ];
    
</script>

<Header></Header>

<div class="corpo-descricao">
    <div class="navbar">
        <span class="inicio">Início</span>
        <img src={arrow_right} alt="Seta p/ direita">
        <span>Pescando um eletricista em Imbiribeira, Recife - PE</span>
    </div>
    <div class="profissional-procurado">
        <span class="header-profissional">Eletricista</span>
        <span class="texto-profissional">Encontre eletricistas qualificados e confiáveis para resolver seus problemas elétricos. Profissionais prontos para atender às suas necessidades de instalação, reparo e manutenção elétrica.</span>
    </div>
    <div class="filtros-profissionais">
        <DropdownMenu/>
    </div>
</div>


<div class="lista-de-cards">
{#each cards as card (card.id)}
        <Card  />
        {/each}
    </div>
  

<style>
    .texto-profissional{
        color: var(--theme-color-dark-gray);
        font-size: 20px;
        font-weight: 400;

    }
    .header-profissional{
        color: var(--theme-text-color-primary);
        font-size: 32px;
        font-weight: 600;

    }
    .profissional-procurado{
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        gap: 5px;
        align-self: stretch;
    }
     
    .inicio{
        color: var(--theme-text-color-secondary) ;
    }
    .navbar{
        display: flex;
        padding: 16px 0px;
        align-items: center;
        gap: 15px;
    }
    .corpo-descricao{
        display: flex;
        width: 1920px;
        padding: 0px 134px;
        flex-direction: column;
        align-items: flex-start;
        gap: 23px;
    }
    .lista-de-cards{
        display: flex;
        flex-direction: row;
        justify-content: center;
        gap: 24px;
        padding: 20px;
        /* justify-content: space-between; */
    }
</style>