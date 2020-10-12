<script>
    import { getContext } from 'svelte';
      import { fly } from 'svelte/transition';
      
    import Popup from './Popup.svelte';
    export let m_message
  
    const { open } = getContext('simple-modal');
      
      
  
    const showPopup = () => {
          open(Popup, { message: `${m_message}` });
      };
  
  </script>
  
  <section>
      <button on:click={showPopup}>Ingredient</button>
      
  
  </section>
  
  <style>
      section {
          padding-top: 0.5em;
      }
      
      
  </style>