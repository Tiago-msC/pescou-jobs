<script>
    import '../../styles.css';
    import Card from '$lib/components/Card.svelte'
    import Header from '$lib/components/Header.svelte'
    import arrow_right from '$lib/assets/icons/slight-arrow-right.svg'
    import DropdownFiltros from '$lib/components/Dropdown-Filtros.svelte';
    import ServiceCategories from '$lib/components/ServiceCategories.svelte'
    const cards = [
    { id: 1, title: 'Card 1' },
    { id: 2, title: 'Card 2' },
    { id: 3, title: 'Card 3' },
    { id: 4, title: 'Card 4' },
  ];
    
</script>

<Header></Header>
<ServiceCategories/>


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
        <DropdownFiltros text="Faixa de preço" text1="R$ 200" text2="R$ 1.000"/>
        <DropdownFiltros text="Distância" text1="Imbiribeira" text2="Londres"/>
        <DropdownFiltros text="Classifição" text1="> 4.5 Estrelas" text2="< 4 Estrelas"/>
        <DropdownFiltros text="Tempo de experiência" text1="< 2 Anos" text2="> 5 Anos"/>
    </div>
</div>

<div class="bloco-inferior">
    <span class="profissionais-achados">20 Eletricistas encontrados em Imbiribeira, Recife, PE</span>
    
    <div class="lista-de-cards">
        {#each cards as card (card.id)}
        <Card  />
        {/each}
    </div>
</div>

<style>
    .profissionais-achados{
        display: flex;
        font-size: 1.125rem;
        font-weight: 500;
        color: var(--theme-color-dark-gray);
        padding: 30px  0px  44px 134px ;
    }
    .filtros-profissionais{
        display: flex;
        align-items: center;
        gap: 30px;
        }
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
        width: auto;
        padding: 0px 134px;
        flex-direction: column;
        align-items: flex-start;
        gap:23px;
        padding-top: 23px;
        padding-bottom: 23px;
        border-bottom: 1px solid var(--theme-color-light-gray);
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