<script lang="ts">
    import Header from '$lib/components/Header.svelte';
    import SlideButton from '$lib/components/SlideButton.svelte';
</script>
<SlideButton>
    <slot/>
</SlideButton>
<Header>
    <slot/>
</Header>