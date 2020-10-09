<script>
    import HeaderBody from '../components/HeaderBody.svelte';
    import MenuBody from '../components/MenuBody.svelte';
    async function fetchCategory(){
        const res = await fetch('http://localhost:4242/menuCategory');
         const data = await res.json();

    if (res.ok) {
      return data;
    } else {
      throw new Error(data);
    }
  }
  
    
    

</script>

<style>
.pa3 {
    padding: 1rem;
}
@media screen and (min-width: 30em) {
    .pa4-ns {
        padding: 2rem;
    }

    .f5-ns {
        font-size: 1rem;
    }
}
.selected {
		background-color: #ff3e00;
		color: white;
	}
</style>


<nav class="pa3 pa4-ns">
{#await fetchCategory()}
    <p>...waiting</p>
    {:then data}
    {#each data.data as item}
        <HeaderBody m_category={item.Category} ></HeaderBody>
    {/each}
    {:catch error}
        <p>An error happened</p>
{/await}
</nav>


<MenuBody></MenuBody>

