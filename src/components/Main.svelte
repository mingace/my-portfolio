<script>
    import Step from "./Step.svelte"

    export let steps = [
        {name: 'Movie-finder', icon: 'fa-solid fa-video'},
        {name: 'Astro-weight Calculator', icon: 'fa-solid fa-earth-americas', href: 'https://astro-weight-calculator.netlify.app'},
        {name: 'San Diego Top Spots', icon: 'fa-solid fa-list', href: 'https://san-diego-top-spots.netlify.app'}
    ]

    let benefits = [
        {name: 'Self-taught Developer', description: 'I am a self-taught developer, mastering coding from free online resources. Started with JavaScript, HTML, CSS, expanded to frameworks, backend, design, and more. I enjoy creative problem-solving for innovative online experiences.'},
        {name: 'Product and UX Enthusiast', description: "Passionate about crafting exceptional user experiences. Immersed in product design, expressing creativity, and mastering new design concepts. Goal is to deliver intuitive and enjoyable online experiences."}, 
        {name: 'Excellent Communicator', description: "Prioritizing transparency and constructive interaction in all aspects of work. Valuing openness and effective communication to build strong relationships and enhance productivity within any team or workspace."},
    ];
</script>

<main class="flex flex-col flex-1 p-4">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
    <section id="introPage" class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14">
        <div class="flex flex-col lg:justify-center text-center lg:left gap-6 md:gap-8 lg:gap-10">
            <h2 class="font-semibold text-3xl sm:text-5xl md:text-6xl">
                Hi, I'm <span class="poppins text-green-400">Nicholas</span> Mingace <br/>Full Stack
                <span class="poppins text-green-400">Developer</span>
            </h2>
            <p class="text-base sm:text-lg md:text-xl">
                My <span class="text-green-400">favorite tech</span> includes JavaScript, TailwindCSS, Node.js + Express.js! I'm currently working on learning Python, SvelteKit, and React.
            </p>
            <button class="mx-auto lg:center text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950">
                <div class="absolute top-0 right-full w-full h-full bg-green-400 opacity-20 group-hover:translate-x-full z-0 duration-200"/>
                <a href="https://www.linkedin.com/in/nicholasmingace" class="relative z-10">Get in touch &rarr;</a>
            </button>            
  
        </div>
        <div class="relative shadow-2xl grid place-items-center">
            <img
                alt="Self.img"
                src={"images/profile2.png"}
                class="object-cover z-[2] max-h-[75vh]"
            />
        </div>
    </section>

    <section id="projects" class="py-20 lg:py-32 flex flex-col gap-24">
        <div class="flex flex-col gap-2 text-center">
            <h6 class="text-lg sm:text-xl md:text-2xl">
                A few of my creative endeavors.
            </h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                Curious to <span class="poppins text-green-400">see</span> my work?
            </h3>
        </div>
        <div class="flex flex-col gap-2 items-center">
            <p class="mx-auto px-4 py-2 rounded-md border border-solid border-white flex items-center gap-2 -mb-4 sm:-mb-0 -mt-10 hover:border-green-700 duration-200">
                <a class="px-4 py-2 text-white-600 hover:text-green-700 duration-200" target="_blank" href="https://www.linkedin.com/in/nicholasmingace"><i class="fa fa-2x fa-linkedin" size="large"></i></a>
                <a class="px-4 py-2 text-white-600 hover:text-green-700 duration-200" target="_blank" href="https://github.com/mingace"><i class="fa fa-2x fa-github"></i></a>
                <a class="px-4 py-2 text-white-600 hover:text-green-700 duration-200" target="_blank" href="https://www.codewars.com/users/nmingace"><i class="fa fa-2x fa-code"></i></a>
            </p>   
        </div>
        <div class="py-5 grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-14">
            <Step step={steps[0]}>
                <p>Movie-finder is an application created with <strong class="text-green-400">Node.js Express.js and OMDB API!</strong> OMDB API is a free API that stores all information on any movie. This project consumes and caches the <strong class="text-green-400">OMDB API</strong> to display box-office statistics of requested movie.</p>
            </Step>
            <Step step={steps[1]}>
                <p>Astro-weight Calculator is an application created with <strong class="text-green-400">HTML5, CSS3, JavaScript, and Regular Expressions!</strong> JavaScript was utilized to implement the dropdown menus and functionality the calculator. RegEx implemented for a fail-catch when wrong inputs were entered.</p>
            </Step>
            <Step step={steps[2]}>
                <p>San Diego Top Spots is an application created with <strong class="text-green-400">HTML5, CSS3, JavaScript, and JavaScript Object Notation!</strong> We were provided a JSON data file and have to append the data to the sheet. Coordinates were given for the project and hyperlinks were implemented to show on Google Maps.</p>
            </Step>
        </div>
    </section>
    <section id="about" class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative">
        <div class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-green-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-green-700 py-4">
            <h6 class="text-lg sm:text-xl md:text-2xl">Want to know more?</h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                A bit <span class="poppins text-green-400">about</span> me.
            </h3>
        </div>
        <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">I am . . .</p>
        <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
            {#each benefits as benefit, index}
                <div class="flex gap-6 sm:gap-8">
                    <p class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-500 font-semibold">
                    #{index+1}
                    </p>
                    <div class="flex flex-col gap-6 sm:gap-8">
                    <h3 class="text-2xl sm:text-3xl md:text-5xl">
                        {benefit.name}
                    </h3>
                        <p>{benefit.description}</p>
                    </div>
                </div>
            {/each}
        </div>
        <h5 class={"text-2xl sm:text-3xl font-semibold text-center poppins"}>The <span class="text-green-400 poppins">Complete</span> Package</h5>
        <div class="flex flex-col overflow-x-scroll gap-10 max-w-[800px] mx-auto w-full">
            <table class="bg-white text-slate-700 rounded text-center">
                <thead class="border-b border-solid border-slate-200">
                    <tr class="">
                        <th/>
                        <th class="whitespace-nowrap p-2 px-4">Candidate #1</th>
                        <th class="whitespace-nowrap p-2 px-4">Candidate #2</th>
                        <th class="whitespace-nowrap p-2 px-4">Candidate #3</th>
                        <th class="whitespace-nowrap bg-green-700 text-white p-4 px-8">Me</th>
                        
                    </tr>
                </thead>
                <tbody>
                    <tr class="border-b border-solid border-slate-200">
                        <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm whitespace-nowrap">Dedication</td>
                        <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-slate-500"></i></td>
                        <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-slate-500"></i></td>
                    </tr>
                    <tr class="border-b border-solid border-slate-200">
                        <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm whitespace-nowrap">Critical Thought</td>
                        <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-slate-500"></i></td>
                    </tr>
                    <tr class="border-b border-solid border-slate-200">
                        <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm whitespace-nowrap">Interpersonal Skills</td>
                        <td><i class="fa-solid fa-check text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-slate-500"></i></td>
                        <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-slate-500"></i></td>
                    </tr>
                    <tr class="border-b border-solid border-slate-200">
                        <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm whitespace-nowrap">Programming Ability</td>
                        <td><i class="fa-solid fa-check text-slate-500"></i></td>
                        <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-slate-500"></i></td>
                    </tr>
                </tbody>
            </table>
        </div>
        <div class="mx-auto -mt-12 italic sm:hidden opacity-50">
            <p>Scroll to see more &rarr;</p>
        </div>
        <h5 class="text-2xl sm:text-3xl font-semibold text-center poppins">So why not <span class="text-green-400 poppins">invest</span>?</h5>
    </section>
</main>