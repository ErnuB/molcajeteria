<script>
    let items = [
        {seccion: 'Entradas', section: 'Apetizers', nombre:'Queso fundido', name: 'Cheese fondue', precio: '110' },
        {seccion: 'Entradas', section: 'Apetizers', nombre:'Queso fundido', name: 'Cheese fondue', precio: '110' },
        {seccion: 'Entradas', section: 'Apetizers', nombre:'Queso fundido', name: 'Cheese fondue', precio: '110' },
        {seccion: 'Entradas', section: 'Apetizers', nombre:'Queso fundido', name: 'Cheese fondue', precio: '110' },
    ];
    
    let english = false;

    function toggleLanguage() {
        english = !english;
    }
</script>

<img src="/img/molcajeteria.png" alt="La Molcajetería" class="m-auto p-5">
<div class="flex flex-col text-5xl gap-10 font-black justify-center text-center">
    <p>Menú</p>
    <p>En Construcción</p>
</div>
<div class="flex justify-center items-center gap-4">
    <span class="font-medium text-gray-700">Español</span>
    <button on:click={toggleLanguage} class="relative inline-flex items-center h-8 rounded-full w-14 bg-blue-400">
        <span class="absolute left-1 transition-transform duration-200 ease-in-out transform bg-white w-6 h-6 rounded-full"
              style:transform="{english ? 'translateX(1.75rem)' : 'translateX(0)'}">
        </span>
    </button>
    <span class="font-medium text-gray-700">English</span>
</div>

{#each items as item}
    {#if english}
        <div class="p-2 text-2xl mx-2">
            <p>{item.section}</p><p>{item.name}</p><p>${item.precio}</p>
        </div>
    {:else}
        <div class="p-2 text-2xl mx-2">
            <p>{item.seccion}</p><p>{item.nombre}</p><p>${item.precio}</p>
        </div>
    {/if}
{/each}

<footer class="fixed bottom-0 bg-ranch w-full font-bebas py-1 bg-slate-400">
    <div class="flex justify-evenly items-center py-1">
        <p class="font-bold text-2xl">Enlaces:</p>
        <a href="https://maps.app.goo.gl/9mxDXSMGWFcfSCJE6" target="_blank"><i class="fa fa-location-dot text-3xl text-red-600"></i></a>
        <a href="https://www.facebook.com/Lamolcajeteriamzt/" target="_top"><i class="text-3xl text-blue-800 fa-brands fa-facebook"></i></a>
        <a href="https://www.instagram.com/lamolcajeteria/" target="_blank"><i class="text-4xl fa-brands fa-square fa-instagram bg-gradient-to-bl from-pink-500 via-red-500 to-yellow-500 text-transparent bg-clip-text"></i></a>
    </div>
</footer>
