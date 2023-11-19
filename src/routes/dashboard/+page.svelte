<script>
    import '../../styles.css';
    import Header from '$lib/components/Header-Prestador-servicos.svelte';
    import Chart from 'chart.js/auto';
    import { onMount } from 'svelte';
    import arrow_right from '$lib/assets/icons/slight-arrow-right.svg';
    import papericon from '$lib/assets/icons/paper-icon.svg';
    import Graphic1 from '$lib/components/graphic1.svelte';
    import Graphic2 from '$lib/components/graphic2.svelte';
    import money_icon from '$lib/assets/icons/money-icon.svg';
    import people_icon from '$lib/assets/icons/people-icon.svg';
    import clipboard_icon from '$lib/assets/icons/clipboard.svg';
</script>

<Header></Header>
<body>
<div class="corposuperior">
  <div class="navbar">
    <span class="inicio"><a href="/">Início</span>
    <img src={arrow_right} alt="Seta p/ direita">
    <span>Meu perfil</span>
    <img src={arrow_right} alt="Seta p/ direita">
    <span><b style="color: var(--theme-text-color-primary);">Dashboard</span>
  </div>
  <div class="titulo-subtitulo">
    <h1 class='titulo'>Dashboard</h1>
    <h3 class='subtitulo'>Revise seus pagamentos e serviços prestados</h3>
</div>

<!-- Sessao dos graficos -->
<div class="sessao-graficos">
  <!-- 1o Grafico  -->
  <div class="dash-servicos-solicitados">
    <div class="head">
      <div class="esquerda">
        <img src={papericon} alt="">
        <span class="texto-head">Numero de serviços solicitados</span>
      </div>
      <div class="filtro-head">
        <select name="filtro" id="filtro" class="filtro">
          <option value="semana">Semana</option>
          <option value="mes">Mês</option>
          <option value="ano">Ano</option>
        </select>
      </div>
    </div>
    <div class="contagem-porcentagem">
      <span class="contagem">10</span>
      <span class="porcentagem">+23.0%</span>
    </div>
    <div class="grafico-servicos-solicitados">
      <Graphic1/>
    </div>
  </div>
  <!-- 2o Grafico -->
  <div class="dash-servicos-solicitados">
    <div class="head">
      <div class="esquerda">
        <img src={money_icon} alt="money_icon">
        <span class="texto-head">Receita total dos serviços</span>
      </div>
      <div class="filtro-head">
        <select name="filtro" id="filtro" class="filtro">
          <option value="semana">Semana</option>
          <option value="mes">Mês</option>
          <option value="ano">Ano</option>
        </select>
      </div>
    </div>
    <div class="contagem-porcentagem">
      <span class="contagem">R$23.490,00</span>
      <span class="porcentagem">+15.0%</span>
    </div>
    <div class="grafico-servicos-solicitados">
      <Graphic2/>
    </div>
  </div>
  <!-- 3o Gráfico -->
  <div class="dash-total-serviçoos-prestados">
    <div class="head">
      <div class="esquerda">
        <img src={clipboard_icon} alt="clipboard_icon">
        <span class="texto-head">Total de serviçoos prestados</span>
      </div>
      <div class="contagem-porcentagem">
        <span class="porcentagem">+8.0%</span>
      </div>
    </div>
    <div class="contagem-servicos">
      <span class="contador-servicos">149</span>
    </div>

    <!-- 4o Grafico -->
  <div class="dash-total-clientes">
    <div class="head">
      <div class="esquerda">
        <img src={people_icon} alt="people_icon">
        <span class="texto-head">Total de clientes</span>
      </div>
      <div class="contagem-porcentagem">
        <span class="porcentagem-negativa">-10.0%</span>
      </div>
    </div>
    <div class="contagem-servicos">
      <span class="contador-servicos">1.549</span>
  </div>
  <!-- Fim da sessao de Gráficos/Dashboard -->
</div>
</body>

<body>
  
  <div class="corpo-inferior">
    <div class="corpo-inferior-esquerda">
      <div class="head-inferior-esquerda">
        <h1>Serviços</h1>
        <h3>Confira os detalhes dos serviços prestados</h3>
      </div>
      <div class="tabela-servicos">

        
      </div>
    </div>


    <div class="corpo-inferior-direito">
      <div class="head-inferior-direita">
        <h1>Feedback</h1>
        <h3>Lista de feedbacks dos seus clientes</h3>
      </div>
      <div class="tabela-feedback">

      </div>
    </div>
  </div>
</body>

<style>
  .tabela-feedback{
    background-color: aliceblue;
    width: 692px;
    height: 694px;
    flex-shrink: 0;
    border-radius: 12px;
    border: 1px solid rgba(120, 120, 133, 0.35);
    box-shadow: 3px 3px 4px 0px rgba(0, 0, 0, 0.082),-1px -1px 4px 1px rgba(0, 0, 0, 0.082);
  }
  .tabela-servicos{
    background-color: aliceblue;
    width: 1087px;
    height: 694px;
    flex-shrink: 0;
    border-radius: 12px;
    border: 1px solid rgba(120, 120, 133, 0.35);
    box-shadow: 3px 3px 4px 0px rgba(0, 0, 0, 0.082),-1px -1px 4px 1px rgba(0, 0, 0, 0.082);
  }
  .head-inferior-direita{
    background-color: aqua;
    margin-bottom: 40px;
  }
  .head-inferior-esquerda{
    background-color: rgb(0, 255, 136);
    margin-bottom: 40px;
  }
  .corpo-inferior{
    display: grid;
    grid-template-columns: 1.7fr 1fr;
    background-color: #f7f7f7;
    width: 100%;
    padding: 25px;
    gap: 40px;
  }



  .porcentagem-negativa{
    background: rgba(238, 68, 58, 0.30);
    border-radius: 15px;
    padding: 8px 16px;
    font-weight: 600;
    display: flex;
    align-items: center;
    margin-left: 75px;
    justify-content: space-between;
    color: #A12626;}
  
  .titulo-subtitulo{
    display: flex;
    flex-direction: column;
    margin-bottom: 32px;
  }
  .dash-total-clientes{
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-top: 100px;
    width: 515px;
    height: 221px;
    padding: 25px;
    border-radius: 12px;
    border: 1px solid var(--theme-border-color-primary);
    box-shadow: 3px 3px 4px 0px rgba(0, 0, 0, 0.082),-1px -1px 4px 1px rgba(0, 0, 0, 0.082);
    overflow: visible;
  }
  .contagem-servicos{
    display: flex;
    margin-top: 20px;
    padding: 20px;
    justify-content: center;
    align-items: center;
    width: 324px;
    height: 73px;
    font-weight: 700;
    background-color: rgba(139, 205, 251, 0.30);
    border-radius: 15px;
  }
  .contador-servicos{

    font-size: 2rem;

  }
  .dash-total-serviçoos-prestados{
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 515px;
    height: 221px;
    padding: 25px;
    border-radius: 12px;
    border: 1px solid var(--theme-border-color-primary);
    box-shadow: 3px 3px 4px 0px rgba(0, 0, 0, 0.082),-1px -1px 4px 1px rgba(0, 0, 0, 0.082);
    overflow: visible;
  }
  .porcentagem{
    background-color: rgba(139, 205, 251, 0.30);
    border-radius: 15px;
    padding: 8px 16px;
    font-weight: 600;
    color: var(--theme-color-primary);

  }
  .contagem{
    font-size: 2rem;
    font-weight: 700;
  }
  .contagem-porcentagem{
    display: flex;
    align-items: center;
    margin-left: 75px;
    margin-bottom: 16px;
    justify-content: space-between;
  }
  .head{
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .filtro{
    width: 110px;
    height: 30px;
    border-radius: 8px;
    border-color: var(--theme-color-light-gray);
    color: var(--theme-text-color-primary);
    font-size: 1rem;
    padding: 0 8px;
  }

  .esquerda{
    display: flex;
    align-items: center;

  }
  .texto-head{
    padding: 15px;
  }
  .esquerda img {
    width: 60px;
    height: 60px;
    padding: 17px;
    border-radius: 15px;
    background: rgba(139, 205, 251, 0.30);
  }
  .dash-servicos-solicitados{
    display: flex;
    flex-direction: column;
    width: 620px;
    height: 507px;
    flex-shrink: 0;
    padding: 25px;
    border-radius: 12px;
    border: 1px solid var(--theme-border-color-primary);
    box-shadow: 3px 3px 4px 0px rgba(0, 0, 0, 0.082),-1px -1px 4px 1px rgba(0, 0, 0, 0.082);
    overflow: visible;

  }
  .sessao-graficos{
    margin-top: 40px;
    margin-bottom: 40px;
    display: flex;
    row-gap: 46px;
    column-gap: 46px;
    /* justify-content: space-between; */
    gap: 32px;
  }

  .subtitulo{
    font-size: 1.25rem;
    font-weight: 400;
    color: var(--theme-text-color-secondary);
    margin-bottom: 32px;
  }
  .titulo{
    font-size: 2.5rem;
    font-weight: 700;
    color: var(--theme-text-color-primary);
    margin-bottom: 8px;
  }
  .corposuperior{
    padding: 56px 60px;
  }
  a{
    text-decoration: none;
    color: var(--theme-text-color-secondary);
  }
  .navbar{
    display: flex;
    /* height: 21px; */
    width:auto;
    margin-bottom: 58px;
    align-items: center;
    gap: 8px;
    font-size: 1rem;
    color: var(--theme-text-color-secondary);
  }
</style>