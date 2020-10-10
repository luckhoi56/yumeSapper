<script>
    import MenuItem from './MenuItem.svelte';
    export let m_category ='Soup';
    let m_items ={"Category": `${m_category}`};
    let promise = getItems();
    async function getItems(){
        const res = await fetch('http://localhost:4242/test1',{
            method:'POST',
            headers:{
                'Content-Type': 'application/json',
            },
            body: JSON.stringify({ Category: 'Soup'})
        });
        const json = await res.json();
        console.log(json)
    }
    
</script>
{#await promise then data}
{#each data.data as item}
<MenuItem m_url={item.Image} m_price={item.Price} m_title={item.ItemName}>

</MenuItem>
{/each}
{/await}

