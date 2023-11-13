<script lang="ts">
    import Button from '$lib/components/Button.svelte';
    import Header from '$lib/components/Header.svelte';
    import SwitchButton from '$lib/components/SwitchButton.svelte';
    import InputServiceLocation from '$lib/components/input-service-location.svelte';
</script>


<Header>
    <slot />
</Header>
<div class="servicelocation">
    <InputServiceLocation>
        <slot />
    </InputServiceLocation>
</div>

<SwitchButton> 
    <slot />
</SwitchButton>

<style>
    .servicelocation{
        padding: auto;
    }
    </style>
 