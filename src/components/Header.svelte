<script>
    import logo from "$lib/images/pescoujobs-logo.svg"
  import Button from "./Button.svelte";
  import account from "$lib/images/icons/account.svg"
</script>

<header>
    <img src={logo} alt="Logo PescouJobs" class="pescoujobs-logo"/>
    <nav>
        <div class="container-nav">
            <ul>
                <li>Para prestadores</li>
                <li>Ajuda</li>
                <li>Cadastrar</li>
            </ul>
            <Button text="Entrar" type="outline" iconLeft={account}></Button>
        </div>
    </nav>
</header>
<style>
    header{
        display: flex;
        justify-content: space-between;
        height: 96px;
        align-items: center;
        padding: 0 48px;
        border-bottom: 1px solid var(--theme-border-color-primary);
        
    }
    ul{
        display: flex;
        margin-right: 24px;
    }
    li{
        list-style: none;   
        margin-left: 34px;

    }
    .container-nav{
        display: flex;
        align-items: center;
    }
    .pescoujobs-logo{
        height: 45px;
        width: 202px;
        object-fit: contain;

    }
</style>
