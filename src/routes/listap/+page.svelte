<script>
  import HeaderSearcher from "$lib/components/Header-Searcher.svelte";
  import arrow_right from "$lib/assets/icons/slight-arrow-right.svg";
  import ServiceCategories from "$lib/components/ServiceCategories.svelte";
  import "../../styles.css";
  import star_active from "$lib/assets/icons/star-avaliation.svg";
  import imagem_perfil from "$lib/assets/image-perfil.svg";
  import verified from "$lib/assets/icons/verified.svg";
  import pin_localizacao from "$lib/assets/icons/pin-localizacao.svg";
  import foto_perfil_grande from "$lib/assets/icons/foto-perfil-grande.svg";
  import Button from "$lib/components/Button.svelte";

  const handleNavigateProfessionals = () => {
    window.location.href = "/profissionais";
  };
</script>

<meta name="viewport" content="width=device-width, initial-scale=1.0" />

<title>Perfil</title>

<HeaderSearcher></HeaderSearcher>
<ServiceCategories />

<body>
  <div class="div-esquerda">
    <div class="head-nav">
      <div class="navbar">
        <span class="inicio">Início</span>
        <img src={arrow_right} alt="Seta p/ direita" />
        <span>Eletricistas</span>
        <img src={arrow_right} alt="Seta p/ direita" />
        <span>Eletricista1002</span>
      </div>
      <div class="profissional-procurado">
        <span class="texto-profissional"
          >Seu eletricista de confiança para iluminar e proteger.</span
        >
        <div class="avaliacao">
          <img src={star_active} alt="Estrela" />
          <span class="numero-avaliacao" style="font-weight: 600;"
            >4.5 <b style="font-weight: 400;color:#777"
              >(<b style="font-weight: 400; text-decoration-line:underline">5</b
              >)</b
            ></span
          >
        </div>
      </div>
    </div>

    <div class="container-foto-nome">
      <img src={foto_perfil_grande} alt="Foto de perfil" />
      <div class="nome-localizacao-botao">
        <div class="foto-nome-verified">
          <span class="nome-prestador">Marcos Antônio</span>
          <img src={verified} alt="Verificado" />
        </div>
        <div class="localizacao">
          <img src={pin_localizacao} alt="" />
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
      <div class="descricao-texto">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Modi quibusdam
        provident illum aut enim praesentium, aspernatur iste cum! Dolorem sunt
        labore incidunt cumque voluptatibus sapiente vitae, sequi deleniti
        accusantium quisquam. Lorem ipsum dolor sit amet consectetur adipisicing
        elit. Ratione libero, error beatae minima voluptatem, nemo deserunt
        porro odio iusto consequuntur pariatur id officia natus rem maxime
        numquam officiis corrupti aut? Lorem, ipsum dolor sit amet consectetur
        adipisicing elit. Dolor temporibus accusantium omnis, aut nemo alias
        iste blanditiis sint maiores fugiat laudantium odit saepe ratione
        quibusdam ad illum quia consectetur at! Lorem ipsum dolor sit amet
        consectetur adipisicing elit. Maxime, dicta, esse voluptatum dolores,
        minus enim reprehenderit non voluptatem tenetur at molestias iure!
        Expedita pariatur itaque nulla, unde inventore fuga in.
      </div>
    </div>
    <div class="tags-relacionadas">
      <div class="tag">
        <span id="tag_texto">Instalação elétrica residencial</span>
      </div>
      <div class="tag">
        <span id="tag_texto">Reparo de circuitos elétricos</span>
      </div>
    </div>


  </div>
  <div class="div-direita">
    <div class="container-agendar">
      <div class="botao1">
        <Button
          expended
          text="Pedir Orçamento"
          type="primary"
          onClick={handleNavigateProfessionals}
        />
      </div>
      <div class="botao2">
        <Button
          expended
          text="Fazer agendamento"
          type="outline"
          onClick={handleNavigateProfessionals}
        />
      </div>
    </div>
    <div class="avaliacoes">
      <h2>Avaliações</h2>
      <div class="container-avaliacao">
        <div class="avaliacao">
          <img src={star_active} alt="Estrela" />
          <span class="numero-avaliacao" style="font-weight: 600;"
            >5 <b style="font-weight: 400;color:#777"
            ></span
          >
          <div class="barra"><div class="preencher"></div></div>
        </div>
        <div class="avaliacao">
          <img src={star_active} alt="Estrela" />
          <span class="numero-avaliacao" style="font-weight: 600;"
            >4 <b style="font-weight: 400;color:#777"
            ></span
          >
          <div class="barra"><div class="preencher" style="width: 11%;"></div></div>
        </div>
        <div class="avaliacao">
          <img src={star_active} alt="Estrela" />
          <span class="numero-avaliacao" style="font-weight: 600;"
            >3 <b style="font-weight: 400;color:#777"
            ></span
          >
          <div class="barra"><div class="preencher" style="width: 7%;"></div></div>
        </div>
        <div class="avaliacao">
          <img src={star_active} alt="Estrela" />
          <span class="numero-avaliacao" style="font-weight: 600;"
            >2 <b style="font-weight: 400;color:#777"></span
          >
          <div class="barra"><div class="preencher" style="width: 4%;"></div></div>
        </div>
        <div class="avaliacao">
          <img src={star_active} alt="Estrela" />
          <span class="numero-avaliacao" style="font-weight: 600;"
            >1 <b style="font-weight: 400;color:#777"
            >
          </span
          >
          <div class="barra"><div class="preencher" style="width: 1%;"></div></div>
        </div>
      </div>
    </div>

  </div>

</body>

<style>
  .container-avaliacao{
    display: flex;
    flex-direction: column;
    margin-top: 20px;
    gap: 15px;
  }
  .avaliacao{
    padding:5px;
  }
  .preencher{
    background: #1dbf73;
    width: 90%;
    height: 5px;
    border-radius: 999px;
  }
  .barra{
    background: #cecece;
    width: 60%;
    height: 5px;
    border-radius: 999px;
  }
  .avaliacoes{
    display: flex;
    padding: 20px;
    flex-direction: column;
    /* align-items: center;
    justify-content: center; */
    border: 1px solid deepskyblue;
    margin-top: 10vmin;
  }
  .botao1,
  .botao2 {
    width: 100%;
  }
  .container-agendar {
    display: flex;
    margin-left: 23%;
    margin-top: 25%;
    gap: 20px;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    width: 60%;
    padding: 23px 19px;
    border-radius: 5px;
    border: 1px solid #cecece;
    background: #fff;
    box-shadow: 0px 2px 3px 1px rgba(0, 0, 0, 0.03);
  }
  .div-direita {
    border: 1px solid #ff9811;
  }
  .div-esquerda {
    border: 1px solid #1dbf73;
  }
  .corpo-descricao {
    display: grid;
    border: 1px solid palegreen;
    /* width: 50%; */
    gap: 30px;
  }
  .tag {
    color: var(--theme-color-text-primary);
    border-radius: 10vmin;
    background: #eee;
    display: flex;
    padding: 10px 16px;
    align-items: center;
    gap: 10px;
  }
  .tags-relacionadas {
    display: flex;
    gap: 10px;
    padding: 20px 0px;
    border: #e4e5e7 1px solid;
  }
  .titulo {
    font-weight: 600;
    font-size: 2rem;
    padding: 10px 0px;
  }
  .localizacao {
    display: flex;
    align-items: center;
    gap: 10px;
    border: #e4e5e7 1px solid;
  }
  .nome-localizacao-botao {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    gap: 8px;
    border: #e4e5e7 1px solid;
  }
  .foto-nome-verified {
    display: flex;
    align-items: center;
    gap: 10px;
    font-size: 1.5rem;
    font-weight: 600;
    border: #e4e5e7 1px solid;
  }
  .container-foto-nome > img {
    width: 12vmin;
    border-radius: 50%;
    border: #e4e5e7 1px solid;
  }
  .container-foto-nome {
    display: flex;
    align-items: center;
    width: 40%;
    justify-content: center;
    width: fit-content;
    gap: 18px;
    padding: 30px 0px;
    border: #4c7ee2 1px solid;
  }
  body {
    padding: 20px 120px;
    background: #131313;
    display: grid;
    grid-template-columns: 1fr 1fr;
  }
  .avaliacao {
    display: flex;
    align-items: center;
    top: 0;
    gap: 10px;
    border: #e4e5e7 1px solid;
  }
  .texto-profissional {
    font-size: 2rem;
    font-weight: 600;
  }
  .profissional-procurado {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    gap: 10px;
    /* width: 60%; */

    border: #1dbf73 1px solid;
  }
  .navbar {
    display: flex;
    padding: 16px 0px;
    align-items: center;
    gap: 15px;
  }
  .head-nav {
    display: flex;
    width: auto;
    /* padding: 0px 134px; */
    flex-direction: column;
    align-items: flex-start;
    gap: 23px;
  }

  @media (max-width: 1024px) {
    .container-agendar {
      margin-top: 45%;
      margin-left: 10%;
      width: 80%;
    }
    .profissional-procurado {
      width: 100%;
      padding: 20px;
    }
    body {
      padding: 30px 30px;
    }
    .container {
      width: 100%;
      max-width: 720px;
    }
    .nome-localizacao-botao {
      padding: 10px;
    }

    @media screen and (max-width: 768px) {
      .container-agendar {
        margin-top: 5%;
        margin-left: 0%;
        width: 100%;
      }
      .div-direita {
        display: block;
        width: 100%;
      }
      body {
        display: block;
      }
      .container-foto-nome {
        display: flex;
        flex-direction: column;
        width: 100%;
      }
      .nome-localizacao-botao .localizacao {
        padding: 10px;
      }
      .nome-localizacao-botao .localizacao,
      .nome-localizacao-botao .foto-nome-verified,
      .nome-localizacao-botao .botao-contato {
        width: 100%;
        justify-content: center;
      }
      .nome-localizacao-botao {
        display: flex;
        flex-direction: column;
        width: 100%;
      }
      .titulo {
        font-size: 1.5rem;
        justify-content: center;
        align-items: center;
        text-align: center;
        padding: 10px;
      }
      .corpo-descricao {
        border-radius: 5px;
        padding: 10px;
        width: 100%;
        height: 200px;
        overflow-y: auto;
      }
      .corpo-descricao::-webkit-scrollbar {
        width: 5px;
      }

      .corpo-descricao::-webkit-scrollbar-track {
        background: var(--theme-color-light-gray);
        height: calc(100%-20px);
        margin: 4px;
      }

      .corpo-descricao::-webkit-scrollbar-thumb {
        background: var(--theme-color-primary);
        border-top-right-radius: 10px;
        border-bottom-right-radius: 10px;
        height: 50px;
      }

      .corpo-descricao::-webkit-scrollbar-thumb:hover {
        background: #555;
      }
      .corpo-descricao .descricao-texto {
        font-size: 1rem;
        position: static;
      }
      .tag {
        font-size: 0.8rem;
      }
      .tags-relacionadas {
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
