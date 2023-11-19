<script>
    import { Chart } from 'chart.js';
    import Servico1 from '$lib/components/Servico1.svelte';
    import '../../styles.css';

</script>

<body>
<div class="caixa-servicos">
    {#each [1,2,3,4,5,6,7,8,9] as id}
    <Servico1 id={id} Texto={id % 4 === 0 ? "Em Andamento" : "Finalizado"}/>
    {/each}
</div>
</body>

<style>
    .caixa-servicos{
        display: flex;
        flex-direction: column;
        padding: 20;
    }
</style>
