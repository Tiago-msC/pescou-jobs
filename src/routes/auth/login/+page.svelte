<script lang="ts">
  import Button from "$lib/components/Button.svelte";
  import logo from "$lib/assets/icons/pescoujobs-logo.svg";
  import { createForm } from 'svelte-forms-lib';

  let errorMessage = '';

  const { form, handleSubmit } = createForm({
    initialValues: {
      email: '',
      password: '',
    },
    onSubmit: values => {
      console.log(values);
    },
  });

  const handleNaviteRegister = () => {
    window.location.href = '/auth/register';
  };

  let processing = false;

  const handleLogin = async () => {
    processing = true;

    await handleSubmit(new Event('submit'));

    setTimeout(() => {
      processing = false;
      errorMessage = "Endereço de e-mail ou senha inválida!"
    }, 1000);
  };

</script>

<svelte:head>
	<title>PescouJobs - Entrar</title>
	<meta name="description" content="Faça login na sua conta do PescouJobs" />
</svelte:head>

<section class="container">
  <div class="container-wrapper">
    <img src={logo} alt="Logo PescouJobs" class="pescoujobs-logo" />
    <h1>Entre em sua conta</h1>
    <p>Um novo jeito de encontrar um prestador de serviços ideal</p>
    <form on:submit|preventDefault={handleSubmit}>
      <div class="form-field">
        <label for="email">E-mail</label>
        <div class:error-color={errorMessage} class="input-container">
          <input name="email" bind:value={$form.email} placeholder="E-mail" type="email" />
        </div>
      </div>
      <div class="form-field">
        <label for="password">Senha</label>
        <div class:error-color={errorMessage} class="input-container">
          <input name="password" bind:value={$form.password} placeholder="Senha" type="password" />
          <div class="bloco" />
        </div>

        {#if errorMessage}
        <div class="erro-senha">
          <span>Endereço de e-mail ou senha inválida!</span>
        </div>
        {/if}

        <div class="form-options-container">
            <Button text="Entrar" expended bind:processing={processing} onClick={handleLogin} />
          <div class="label-or">
            <span> Ou </span>
          </div>
          <Button text="Criar uma Conta" expended type="outline" onClick={handleNaviteRegister} />
        </div>
      </div>
    </form>
  </div>
</section>

<style>
  .pescoujobs-logo {
    height: 40px;
    object-fit: contain;
  }

  

  section.container {
    height: calc(100% - 96px);
    display: flex;
    flex-direction: row;
    justify-content: center;
  }
  .container-wrapper {
    height: 520px;
    width: 520px;
    margin: 0 16px;
    margin-top: 150px;
  }

  img + h1 {
    color: #000000;
    font-weight: 600;
    font-size: 1.5rem;
    margin-top: 12px;
  }

  h1 + p {
    color: #777777;
    font-family: "Poppins-Regular";
    font-size: 0.875rem;
    font-weight: 400;
    margin-top: 8px;
  }

  form {
    margin-top: 36px;
  }
  .form-field {
    display: block;
    margin-bottom: 16px;
  }
  label {
    color: #000000;
    font-size: 0.875rem;
  }

  input {
    display: block;
    /* background-color: greenyellow; */
    border: 0;
    outline: none;
    /* background-color: transparent; */
    width: 100%;
  }
  .input-container {
    /* background-color: red; */
    border: 1px solid #cecece;
    padding: 13px 16px;
    margin-top: 5px;
    display: flex;
  }

  /* .input-container:focus-within{
    transition: 0.5s;
    border: 1px solid #000000;
} */
  .input-container:focus-within {
    transition: 0.5s;
    border: 1px solid var(--theme-color-secondary);
  }

  .error-color {
    border: 1px solid var(--theme-color-red);
  }

  .erro-senha {
    /* visibility: hidden; */
    margin-top: 8px;
    font-size: 0.875rem;
    color: var(--theme-color-red);

    font-weight: 500;
    line-height: normal;
  }

  .label-or {
    display: flex;
    justify-content: center;
    align-items: center;
    margin: 12px 0;
  }

  .form-options-container {
    margin-top: 24px;
  }

</style>
