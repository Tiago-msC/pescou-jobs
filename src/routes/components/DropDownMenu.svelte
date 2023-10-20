<title>DropDown Menu</title>

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

<body>
    <nav >
        <ul >
            <li class="dropdown">
                <a href='#'>Para prestadores <i class="fas fa-chevron-down" style="color: #a9a9a9; font-size: 12;"></i></a>
                <div class="menu">
                    <a href="#">Área do prestador </a> 
                    <a href="#">Torne-se um prestador</a> 
                </div>
            </li>

        </ul>
    </nav>
</body>

<style>
   
    nav{
        margin: 0;
        padding: 0;

        font-family: 'Poppins';
        font-style: normal;
        font-weight: 400;
        font-size: 16px;
        line-height: 24px;


        border: 0;
        outline: 0;
        }
    
    .dropdown{
        display: inline-block;
        position: absolute;
    }

    .dropdown:hover .menu{
        display: block;
        }

    .dropdown a{
        color:black;
        text-decoration: none;
        padding-right: 30;

        display: block;
        padding: 10;
    }

    .menu{
        box-shadow: 1px 1px 6px #b0b0b0;
        border-radius: 3px;
        display: none;
    }