<script>
  import Step from "./Step.svelte";
  let steps = [
    {name:'firefly', icon: 'fa-solid fa-cart-shopping'},
    {name:'superman', icon: 'fa-solid fa-list-check'},
    {name:'batcave', icon: 'fa-solid fa-diagram-project'}
  ]

  let benefits = [
    {name:'university student', description:''},
    {name:'baseball player', description:''},
    {name:'love blackjck', description:''},
  ]
</script>

<main class="flex flex-col flex-1 p-4">
  <section id="introPage" class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 s,:py-14">
    <div class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10">
      <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
        Hi! I'm <span class="poppins text-violet-400">Chris </span>Liang
        <br>Full stack
        <span class="poppins text-violet-400">Developer</span>
      </h2>
      <p class="text-base sm:text-lg md:text-xl">
        My <span class="text-violet-400">favorite tech</span> is Svelte
      </p>
      <a href="https://www.linkedin.com/in/xianmai-chris-liang-9b84b5253/" target="_blank" class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950">
        <div class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200 cursor-pointer">

        </div>
        <h4 class="relative z-9">Get in Touch &rarr;</h4>

      </a>

    </div>
    <div class="relative shadow-2xl grid place-items-center">
      <img src={"images/me.jpg"} alt="Profile images" class="object-cover z-[2] max-h[70vh]">
    </div>

  </section>
  <section id="projects" class="py-20 lg:py-32 flex flex-col gap-24">
    <div class="flex flex-col gap-2 text-center">
      <h6 class="text-lg sm:text-xl md:text-2xl">
        a few of my creative endeavors
      </h6>
      <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
        curious to <span class="poppins text-violet-400"> see </span> my work?
      </h3>
      

    </div>
    <a href="http://google.com" target="_blank" class="mx-auto px-4 py-2 rounded-md border border-solid border-white flex items-center gap-2 -mb-4 sm:-mb-0 -mt-10 hover:border-l-violet-700 duration-200">
      <i class="fa-regular fa-circle-play"/>
      <p>watch the video</p>
    
    </a>
    <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-12">
      <Step step={steps[0]}>
        <p>firely just cuz I thouht of it <strong class="text-violet-400">Next.js stripe and node.js</strong></p>

      </Step>
      <Step step={steps[1]}>
        <p>superman is a DC hero <strong class="text-violet-400">Not</strong> my Fav</p>

      </Step>
      <Step step={steps[2]}>
        <p><strong class="text-violet-400">Love</strong> batcave</p>
      </Step>
    </div>
  </section>

  <section id="about" class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative">
    <div class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700 after:absolute after:bottom-0 after:right-0 
    after:w-2/3 after:h-1.5 after:bg-violet-700 py-4">
    <h6 class="text-lg sm:text-xl md:text-2xl">want to know more?</h6>
    <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">a bit <span class="poppins text-violet-400">about</span> me</h3>
  </div>
  <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">I am ....</p>
  <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
    {#each benefits as benefit, index}
    <div class="flex gap-6 sm:gap-8">
      <p class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-500 font-semibold">
        0{index+1}
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
  <h5 class="text-2xl sm:text-3xl font-semibold text-center poppins">The <span class="text-violet-400">Complete</span> Package wink</h5>
  <div class="flex flex-col overflow-x-scroll gap-10 max-w-[800px] mx-auto w-full">
    <table class="bg-white text-slate-700 rounded text-center">
      <thead class="border-b border-solid border-slate-200">
        <tr class="">
          <th />
          <th class="whitespace-nowrap p-2 px-4">candidate #1</th>
          <th class="whitespace-nowrap p-2 px-4">candidate #2</th>
          <th class="whitespace-nowrap p-2 px-4">candidate #3</th>
          <th class="whitespace-nowrap bg-violet-700 text-white p-4 px-8">me</th>
        </tr>

      </thead>
      <tbody>
        <tr class="border-b border-solid border-slate-200">
          <td class="border-r border-solit border-white pl-4 pr-8 py-4 font-semibold text-sm">
            defication
          </td>
          <td><i class="fa-solid fa-xmark text-slate-500"/></td>
          <td><i class="fa-solid fa-xmark text-slate-500"/></td>
          <td><i class="fa-solid fa-xmark text-slate-500"/></td>
          <td><i class="fa-solid fa-check text-slate-500"/></td>
        </tr>
        <tr class="border-b border-solid border-slate-200">
          <td class="border-r border-solit border-white pl-4 pr-8 py-4 font-semibold text-sm">
            critcal thought
          </td>
          <td><i class="fa-solid fa-xmark text-slate-500"/></td>
          <td><i class="fa-solid fa-xmark text-slate-500"/></td>
          <td><i class="fa-solid fa-xmark text-slate-500"/></td>
          <td><i class="fa-solid fa-check text-slate-500"/></td>
        </tr>
        <tr class="border-b border-solid border-slate-200">
          <td class="border-r border-solit border-white pl-4 pr-8 py-4 font-semibold text-sm">
            wink
          </td>
          <td><i class="fa-solid fa-xmark text-slate-500"/></td>
          <td><i class="fa-solid fa-xmark text-slate-500"/></td>
          <td><i class="fa-solid fa-xmark text-slate-500"/></td>
          <td><i class="fa-solid fa-check text-slate-500"/></td>
        </tr>
      </tbody>
      <tr class="border-b border-solid border-slate-200">
        <td class="border-r border-solit border-white pl-4 pr-8 py-4 font-semibold text-sm">
          wink wink
        </td>
        <td><i class="fa-solid fa-xmark text-slate-500"/></td>
        <td><i class="fa-solid fa-xmark text-slate-500"/></td>
        <td><i class="fa-solid fa-xmark text-slate-500"/></td>
        <td><i class="fa-solid fa-check text-slate-500"/></td>
      </tr>

    </table>
  </div>
  <div class="mx-auto -mt-12 italic sm:hidden opacity-50">
    <p>scroll to see more &rAarr;</p>
  </div>
  <p class="mx-auto text-2xl sm:text-3xl font-semibold text-center poppins">invest</p>
  </section>
</main>