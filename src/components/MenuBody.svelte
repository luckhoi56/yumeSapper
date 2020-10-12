<script>
    import MenuItem from './MenuItem.svelte';
    import Modal from './modal_essential/Modal.svelte';
    export let m_category ='';
    
    let promise = getItems(m_category);
    async function getItems(m_category){
        const res = await fetch('http://localhost:4242/test1',{
            method:'POST',
            headers:{
                'Content-Type': 'application/json',
            },
            //body: JSON.stringify({ Category: 'Smoothie'})
            body: JSON.stringify({ Category: `${m_category}`})
        });
        const json = await res.json();
        console.log(json)
        return json;
    }
    
</script>
<style>
.cf:before, .cf:after {
    content: " ";
    display: table;
}

.cf:after {
    clear: both;
}

.cf {
    *zoom: 1;
}

.fl {
    float: left;
    _display: inline;
}

.w-50 {
    width: 50%;
}

.bg-light-gray {
    background-color: #eee;
}

.bg-near-white {
    background-color: #f4f4f4;
}

.tc {
    text-align: center;
}
</style>

{#await promise then data}
<div class="cf">
{#each data.data as item}
<div class="fl w-50 bg-near-white tc">
<Modal>
    <MenuItem m_url={item.Image} m_price={item.Price} m_title={item.ItemName}>

    </MenuItem>
</Modal>

</div>

{/each}
</div>
{/await}

