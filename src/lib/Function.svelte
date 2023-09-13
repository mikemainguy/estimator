<script>
    import { createEventDispatcher} from "svelte";
    const dispatch = createEventDispatcher();
    function addWorkItem() {
        dispatch('message', {item: document.querySelector('#workitem').value});
    }
</script>
<h3>Epic</h3>
<textarea id="workitem" rows="10">

</textarea>
<button on:click={addWorkItem}>Add</button>
<style>
    textarea {
        width: 100%;
        height: 100%;
    }
</style>
