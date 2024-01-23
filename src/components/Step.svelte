<script>
    export let step
</script>

<a href={step.href} target="_blank" class="p-4 sm:p-6 md:p-8 flex flex-col gap-4 rounded-lg border border-solid border-green-700 text-center cursor-pointer duration-200 relative">
    <div class="bg-slate-950 grid place-items-center px-4 text-5xl md:text-6xl -mt-10 sm:-mt-12 md:-mt-14 lg:-mt-16 mx-auto duration-200">
        <i class={step.icon}></i>
    </div>
    <h3 class="font-medium text-xl sm:text-2xl md:text-3xl">{step.name}</h3>
    <slot/>
    <div class="flex-1 flex flex-col-reverse sm:flex-row sm:justify-center gap-4 items-end">
        <span class="blueShadow text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-4 py-3 mt-4 group rounded-full bg-white text-slate-950 cursor-pointer">
            <div class="absolute top-0 right-full w-full h-full bg-green-400 opacity-20 group-hover:translate-x-full z-0 duration-200"/>
            <p>Live &rarr;</p>
        </span>
    </div>
</a>







