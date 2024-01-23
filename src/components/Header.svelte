<script>
    export let y;

    export let tabs = [
        {name: 'Projects', link: "#projects"},
        {name: 'About me', link: "#about"},
        ]; 

        function goTop() {
        document.body.scrollIntoView();
        } 
</script>
<header class="{`sticky z-[20] top-0 duration-200 px-5 flex items-center justify-between border border-solid ${y > 0 ? 'py-4 bg-slate-950 border-green-950' : 'py-6 bg-transparent border-transparent'}`}">
    <button on:click={goTop}>
        <img alt="Logo" src="images/logo.png" class="h-17 w-40"/>
    </button>

    <div class="sm:flex items-center gap-4 hidden">
        {#each tabs as { link, name }, index}
            <a href={link} class="duration-200 hover:text-green-400">
                <p>{name}</p>
            </a>
        {/each}
    </div>
</header>
