<title>DropDown Menu</title>
<script lang="ts">
    export let text: string = "";
    export let text1: string = "";
    export let text2: string = "";
    
    import downarrow from '$lib/assets/icons/downarrow.svg'
</script>
<div>
    <nav >
        <div class="dropdown-filtro">
            <ul >
                <li class="dropdown">
                    <a href='#'><b>{text}</b> <i class="fas fa-chevron-down" style="color: #a9a9a9; font-size: 12;"></i></a>
                    <div class="menu">
                        <a href="#">{text1}</a> 
                        <a href="#">{text2}</a> 
                    </div>
                    <img src={downarrow} alt="">
                </li>
            </ul>
        </div>
    </nav>
</div>

<style>
   
   .dropdown{
    display: flex;
    padding: 4px 16px;
    align-items: center;
    gap: 10px;
    border: 1px solid var(--theme-color-light-gray);
    background: var(--theme-color-white);
    position: relative;
}

.dropdown:hover .menu{
    display: inline-block;
    padding: 10px;
    
}

.dropdown a{
    color:black;
    text-decoration: none;
    padding-right: 30;
    text-align: justify;
    display: block;
    padding: 10px;
}

.menu{
    border: 1px solid var(--theme-color-light-gray);
    background: var(--theme-color-white);
    display: none;
    position: absolute; 
    top: 100%; 
    left: 0; 
    width: 100%;
    
}
    </style>