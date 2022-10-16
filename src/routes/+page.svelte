<script>
// @ts-nocheck


import { pokemon } from "../stores/PokeStore"
import PokemonCard from '../components/PokemanCard.svelte'
let searchtext=''

let filtredPokemon=[]

$:{


    if (searchtext) {
       filtredPokemon = $pokemon.filter( pokeman => 
        pokeman.name.toLowerCase().includes(searchtext.toLowerCase())
       
        )
        
    }
    else{
        filtredPokemon=[...$pokemon]
    }
}

</script>
<svelte:head>
    <title>PokeIndex</title>
</svelte:head>



<h1 class="text-4xl text-center my-8 uppercase">podex</h1>



    <input type="text"
    class="p-3 w-full  text-xl border border-dark-100 rounded-lg"  
    placeholder="search pokemon" 
    bind:value={searchtext}
    
    >

<div class=" py-4 grid gap-4 lg:grid-cols-3  md:grid-cols-2 grid-cols-1">

    {#each filtredPokemon as pokemon}
    
    <PokemonCard pokeman={pokemon} />
    {/each}
</div>