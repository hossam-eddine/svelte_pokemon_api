

<script>
// @ts-nocheck

export let data
</script>
<div class="p-6 flex  flex-col  my-10  items-center 
   w-64 h-65 border-4 border-orange-700
     mx-auto 
     bg-gray-100 rounded-lg
      hover:bg-gray-200 hover:shadow-lg
      cursor-pointer
       ">

    <img class="w-40 h-40" src={data.pokeman.sprites['front_default']} alt={data.pokeman.name}>
    <h1 class="text-2xl text-center my-8 uppercase">{data.pokeman.name}</h1>
    <p><strong>Type:</strong> {data.pokeman.types[0].type.name}</p>
    <p><strong>Height: </strong>{data.pokeman.height} || <strong>Weight</strong>{data.pokeman.weight} kg </p>
</div>

