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
        <h1>Entre em sua conta</h1>
        <p>Um novo jeito de encontrar um prestador de serviços ideal</p>
        <form action="">
          <div class="form-field">
            <label for="email">E-mail</label>
            <div class="input-container">
              <input name="email" placeholder="E-mail"type="email" required />
            </div>
          </div>
          <div class="form-field">
            <label for="password">Senha</label>
            <div class="input-container">
              <input name="password" placeholder="Senha"type="password" required />
              <div class="bloco"></div>
            </div>
            <div class="erro-senha">
              <span>Endereço de e-mail ou senha inválida!</span>
            </div>
            <div class="button button-primary" >
              <span>Entrar</span>
            </div>
            <div class="label-or">
              <span>
                Ou
              </span>
            </div>
            <div class="button button-outline">
              <span>Criar uma conta</span>
            </div>
          </div>
        </form>
      </div>
    </section>


  </body>
</html>
