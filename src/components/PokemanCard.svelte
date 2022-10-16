<script>
// @ts-nocheck

 import { fade } from "svelte/transition";
    
    export let pokeman;
</script>

<a transition:fade  href={`pokemon/${pokeman.id}`} class="p-6 flex flex-col text-center items-center bg-gray-100 rounded-md hover:bg-gray-300">

    <img src={pokeman.image} alt={pokeman.name} class="h40 w-40" >
    <h2 class="text-2xl uppercase">{ pokeman.id } .{pokeman.name}</h2>
</a>