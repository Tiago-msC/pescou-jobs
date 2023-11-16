<script>
  import logo from "$lib/assets/icons/pescoujobs-logo.svg";
  import logoRetractable from "$lib/assets/icons/pescoujobs-logo-retractable.svg";
  import Button from "./Button.svelte";
  import account from "$lib/assets/icons/account.svg";

  const handleNavigateLogin = () => {
    window.location.href = "/auth/login";
  };

</script>

<header>
  <!-- <img src={logoRetractable} alt="Logo PescouJobs" class="pescoujobs-logo-retractable"/> -->
  <nav id="desktop-menu">
    <img src={logo} alt="Logo PescouJobs" class="pescoujobs-logo" />
    <div class="container-nav">
      <ul>
        <li><a href="/">Para prestadores</a></li>
        <li><a href="/">Ajuda</a></li>
        <li><a href="/">Cadastrar</a></li>
      </ul>
      <Button
        text="Entrar"
        notClickAnimation
        type="outline"
        iconLeft={account}
        onClick={handleNavigateLogin}
      />
    </div>
  </nav>
  <nav id="mobile-menu">
    <img src={logoRetractable} alt="Logo PescouJobs" class="pescoujobs-logo-retractable" />
  </nav>
</header>

<style>
  header {
    border-bottom: 1px solid var(--theme-border-color-primary);
  }

  nav {
    height: 96px;
    padding: 0 48px;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  #mobile-menu {
    display: none;
  }

  ul {
    display: flex;
    margin-right: 24px;
  }
  li {
  list-style: none;
  margin-left: 34px;
  position: relative; 
  }

  li::after {
    content: "";
    position: absolute;
    bottom: -1px;
    left: 0;
    width: 0;
    height: 1px;
    background-color: var(--theme-text-color-primary);
    transition: width 0.4s; 
  }


  li:hover::after {
    width: 100%; 
  }

  .container-nav {
    display: flex;
    align-items: center;
  }
  .pescoujobs-logo,
  .pescoujobs-logo-retractable {
    height: 40px;
    object-fit: contain;
  }

  .pescoujobs-logo-retractable {
    display: none;
  }
  a {
    text-decoration: none;
    color: var(--theme-text-color-primary);
    font-size: 0.9rem;
    font-weight: 500;
  }

  @media (max-width: 768px) {
    nav {
      padding: 0 24px;
    }

    ul {
      display: none;
    }
  }

    @media (max-width: 480px) {
        header{
            padding: 0 16px;
            justify-content: center;
        }

        #desktop-menu{
            display: none;
        }

        #mobile-menu{
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .pescoujobs-logo-retractable {
            display: block;
        }
    }
</style>
