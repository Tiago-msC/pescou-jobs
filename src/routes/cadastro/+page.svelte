<!DOCTYPE html>
<html lang="pt-br">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Página de Login</title>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <header id="header-login">
      <div class="header-container">
        <div class="bloco"></div>
      </div>
    </header>
    <section class="container">
      <div class="container-wrapper">
        <h1 id="logo">Logo</h1>
        <h1>Cadastre-se agora mesmo</h1>
        <p>Um novo jeito de encontrar um prestador de serviços ideal</p>
        <form action="">
          <div class="form-field">
            <label for="nome-completo">Nome completo</label>
            <div class="input-container">
              <input name="nome-completo" placeholder="Insira seu nome completo"type="email" required />
            </div>
            <label for="email">E-mail</label>
            <div class="input-container">
              <input name="email" placeholder="Insira o seu E-mail"type="email" required />
            </div>
          </div>
          <div class="form-field">
            <label for="password">Senha</label>
            <div class="input-container">
              <input name="password" placeholder="Insira a sua senha"type="password" required />
              <div class="bloco"></div>
            </div>
            <div class="erro-senha">
              <span>Senha muito fraca!</span>
            </div>
            <div class="button button-primary" >
              <span>Criar uma conta</span>
            </div>
            <div class="label-or">

          </div>
        </form>
      </div>
    </section>

    <!-- <script src="index.js"></script>
    <div class="container">
      <div class="header">
        <h1 class="logo">LOGO</h1>
        <h2 class="title">Entre em sua conta</h2>
        <p class="subtitle">
          Um novo jeito de encontrar um prestador de serviço ideal
        </p>
      </div>
      <div class="form">
        <label class="Email">E-mail</label>
        <input type="email" placeholder="E-mail" required />
        <label class="Senha">Senha</label>
        <input type="password" placeholder="Senha" required />
        <button id="buttonEntrar" type="submit">Entrar</button>
        <button id="buttonCadastro" type="submit">Criar uma conta</button>
        <p class="create-account">Ainda não tem uma conta? <a href="#">Criar uma conta</a></p>
      </div>
</div> -->
  </body>
</html>
