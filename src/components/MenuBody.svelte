<script>
    import MenuItem from './MenuItem.svelte';
    import { onMount } from "svelte";
    const apiURL = "http://localhost:4242/menu";
    let data = [];
    const promise = fetch(apiURL).then(response => response.json());
    
</script>
{#await promise then data}
{#each data.data as item}
<MenuItem m_url={item.Image} m_price={item.Price} m_title={item.ItemName}>

</MenuItem>
{/each}
{/await}

