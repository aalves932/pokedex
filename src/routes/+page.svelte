<script>
// @ts-nocheck

    /** This is the MAIN page*/
    import {pokemon} from "../stores/pokestore"
    import PokemanCard from "../components/pokemanCard.svelte";

    let searchTerm = ""
    // @ts-ignore
    let filteredPokemon = []

    $: {
        if (searchTerm) {
            filteredPokemon = $pokemon.filter( pokeman => {
                return pokeman.name.toLowerCase().includes(searchTerm.toLowerCase())
            })
            console.log(searchTerm);
        }else{
            filteredPokemon = [...$pokemon]
        }
    }
 
</script>

<svelte:head>
    <title>Pokedex</title>
</svelte:head>

<h1 class="text-4xl text-center my-8">Svelte Kit Pokedex</h1>

<input class="w-full rounded-md text-base p-4 border-gray-800" type="text" bind:value={searchTerm} placeholder="encontre seu pokemon">

<div class="py-4 grid gap-4 md:grid-cols-4 grid-cols-2">
    {#each filteredPokemon as pokeman}
    <PokemanCard pokeman={pokeman}/>
    {/each}
</div>