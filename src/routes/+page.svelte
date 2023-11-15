<script lang="ts">

    import Button from '$lib/components/Button.svelte';
    import Header from '$lib/components/Header.svelte';
    import arrowicon from '$lib/assets/icons/arrow-right.svg';
    import InputServiceLocation from '$lib/components/input-service-location.svelte';
</script>

<svelte:head>
	<title>PescouJobs - Encontre profissionais Qualificados</title>
	<meta name="description" content="Encontre profissionais Qualificados">
</svelte:head>

<Header />

<div class="background">
  <div class="corpo">
      <div class="header-bloco">
          <div class="texto-head" >
              <div>
                  <span style="font-size: 48px; font-weight: bolder; color:var(--theme-color-secondary)">Encontre profissionais Qualificados</span>
              </div>
              <div class="subheader">
                  <span >Busque por <b style="color: var(--theme-color-secondary)">serviço</b> e  <b style="color: var(--theme-color-secondary)">profissionais</b> confiáveis perto de você.</span>
              </div>
              <div class="servicelocation">
                  <InputServiceLocation />
              </div>
              
          </div>

          <a href="./Listagem" style="text-decoration: none;"><div class="button-finder" style="width: 710px; ">
              <Button
              iconRight={arrowicon}
              expended
              text="Buscar profissionais"
              type="primary"
          />
          
          </div></a>
      </div>
  </div>
  
</div>

  <style>
      .subheader{
          margin-top: 16px;
          margin-bottom: 24px;
          color: #787878;
          font-size: 20px;
          font-weight: 400;   
      }
      .corpo{
          display: flex;
          width: 774px;
          padding: 48px 32px;
          flex-direction: column;
          align-items: flex-start;
          gap: 10px;
          background-color: #ffffff;
          border-radius: 5px;
          box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);

      }
      .background{
          background-image: url(src/lib/assets/foto-back.png);
          padding: 80px 100px 100px 100px;
          background-position: -25vw;
          background-repeat: no-repeat;
          background-size: cover; 

      }
      .servicelocation{
          margin-left: -20px;
      }
      </style>