<script lang="ts">
    import { createEventDispatcher } from "svelte";
    const dispatch = createEventDispatcher();
    export let name: string = "world!";

    const handleClick = () => {
        dispatch('message', name)
    }
</script>

<button on:click={handleClick}>hello {name}</button>
