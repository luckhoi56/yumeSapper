<script>
    import Content from './modal_essential/Content.svelte';
    import Modal from './modal_essential/Modal.svelte';
   export let m_content;
</script>


<Modal>
    <Content m_message ={m_content}></Content>
</Modal>