<script lang="ts">
  import Button from "$lib/components/Button.svelte";
  import Header from "$lib/components/Header.svelte";
  import arrowicon from "$lib/assets/icons/arrow-right.svg";
  import InputServiceLocation from "$lib/components/input-service-location.svelte";
  import backgroundImage from "$lib/assets/foto-back.png";
</script>

<svelte:head>
  <title>PescouJobs - Encontre profissionais Qualificados</title>
  <meta name="description" content="Encontre profissionais Qualificados" />
</svelte:head>

<Header />

<img src={backgroundImage} alt="Logo PescouJobs" class="background-image-responsive" />

<div class="background" style="background-image: url({backgroundImage})">
  <div class="corpo">
    <div class="header-bloco">
      <div class="texto-head">
        <span
          >Encontre profissionais Qualificados</span
        >
        <div class="subheader">
          <span
            >Busque por <b style="color: var(--theme-color-secondary)"
              >serviço</b
            >
            e <b style="color: var(--theme-color-secondary)">profissionais</b> confiáveis
            perto de você.</span
          >
        </div>
        <div class="servicelocation">
          <InputServiceLocation />
        </div>
      </div>

      <a href="./Listagem" style="text-decoration: none;"
        ><div class="button-finder">
          <Button
            iconRight={arrowicon}
            expended
            text="Buscar profissionais"
            type="primary"
          />
        </div>
      </a>
    </div>
  </div>
</div>

<style>
  .subheader {
    margin-top: 16px;
    margin-bottom: 24px;
    color: #787878;
    font-size: 1rem;
    font-weight: 400;
  }

  .background-image-responsive {
    display: none;
  }

  .header-bloco {
    width: 100%;
  }

  div.texto-head > span {
    font-size: 2.5rem; 
    font-weight: 600; 
    color: var(--theme-color-secondary)
  }
  .corpo {
    display: flex;
    max-width: 680px;
    padding: 48px 32px;
    flex-direction: column;
    align-items: flex-start;
    background-color: #ffffff;
    border-radius: 5px;
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
  }
  .background {
    width: 100%;
    /* background-image: url({backgroundImage}); */
    padding: 80px 100px 100px 100px;
    /* background-position: -25vw; */
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
  }
  /* .servicelocation {
    margin-left: -20px;
  } */

  @media (max-width: 900px) {
    .background-image-responsive {
        display: block;
        width: 100%;
        height: 350px;
        object-fit: cover;
    }
    .background {
        padding: 0px;
        background-image: none !important;
    }

    .corpo {
        /* width: 100%; */
        border-radius: 0px;
        box-shadow: none;
    }
  }

  @media (max-width: 768px) {
    .background-image-responsive {
        display: block;
        width: 100%;
        height: 250px;
        object-fit: cover;
    }

    .background {
        padding: 0px;
        background-image: none !important;
    }

    .corpo {
        /* width: 100%; */
        border-radius: 0px;
        box-shadow: none;
    }
  }
</style>
