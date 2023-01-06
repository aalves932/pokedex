<script>
    export let pokeman={};
</script>

<a class="p-6 bg-gray-100 text-gray-800 
          rounded-md shadow-sm hover:shadow-md flex 
          flex-col items-center" href={`/pokemon/${pokeman.id}`}>

    <h1 class="uppercase text-xl text-left">{pokeman.id}</h1>
    <img class="h-40 w-40" src={pokeman.image} alt={pokeman.name}>
    <h2 class="uppercase text-base">{pokeman.name}</h2>
</a>