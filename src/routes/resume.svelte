<script>
  import { onMount } from 'svelte';
	let StackOverFlowCount = '-1';
  let reposCount = '...'
	
	function handleMouseOver(e) {
		StackOverFlowCount = '😉';
	}
	function handleMouseOut(e) {
		StackOverFlowCount = '-1';
	}

  async function fetchReposCount() {
			const repos = await fetch(`https://api.github.com/users/Beenyaa/repos`).then(r => r.json());
      reposCount = repos.length
		}

	onMount(fetchReposCount);
</script>


<section class="pt-16">
<div class="container lg:w-10/12 px-4 mx-auto">
  <div class="relative flex flex-col min-w-0 break-words bg-white/[.62] dark:bg-slate-800/[.62] backdrop-filter backdrop-blur-xl w-full mb-6 dark:shadow-slate-800 shadow-xl rounded-lg mb-16">
    <div class="px-6">
      <div class="flex flex-wrap justify-center">
        <div class="w-full flex justify-center">
          <div class="mb-12">
            <img alt="..." src="/me.webp" class="dark:shadow-slate-800 shadow-lg rounded-full h-auto align-middle border-none absolute -m-16 -ml-20 lg:-ml-16 h-36 w-36 max-w-36">
          </div>
        </div>
        <div class="text-center mt-12">
          <h3 class="text-xl font-semibold leading-normal mb-2 text-slate-700 dark:text-white mb-2">
            Bence Gadányi
          </h3>
          <div class="text-sm leading-normal mt-0 mb-2 text-slate-400 font-bold uppercase">
            <i class="fas fa-map-marker-alt mr-2 text-lg text-slate-400"></i>
            Leeds, UK
          </div>
          <div class="mb-2 text-slate-600 dark:text-white mt-10">
            <i class="fas fa-briefcase mr-2 text-lg text-slate-400"></i>
            Full-Stack Engineer @ <a class="external-frontpage underline" href="https://www.equans.co.uk/" rel="noreferrer" target="_blank">Equans</a>
          </div>
          <div class="mb-2 text-slate-600 dark:text-white">
            <i class="fas fa-university mr-2 text-lg text-slate-400"></i>
            First Class Computer Science (BSc)
          </div>
        </div>
        <div class="w-full px-4 text-center">
          <div class="flex justify-center py-4 lg:pt-4 pt-8">
            <div class="mr-4 p-3 text-center">
              <span class="text-xl font-bold block uppercase tracking-wide text-slate-600 dark:text-white">
                0
              </span>
              <span class="text-sm text-slate-400">Projects</span>
            </div>
            <div class="mr-4 p-3 text-center">
              <span class="text-xl font-bold block uppercase tracking-wide text-slate-600 dark:text-white dark:text-white">
                {reposCount}
              </span>
              <span class="text-sm text-slate-400">Github <br/>Public Repos</span>
            </div>
            <div class="lg:mr-4 p-3 text-center">
              <span class="text-xl font-bold block uppercase tracking-wide text-slate-600 dark:text-white" on:mouseover={handleMouseOver} on:mouseout={handleMouseOut}>
                {StackOverFlowCount}
              </span>
              <span class="text-sm text-slate-400">Stack Overflow <br/>Upvotes</span>
            </div>
          </div>
        </div>
      </div>
      <div class="py-10 border-t border-slate-200 dark:border-slate-500 text-justify">
        <div class="flex flex-wrap justify-center">
          <div class="w-full lg:w-9/12">
            <p class="mb-4 md:text-lg leading-relaxed text-slate-700 dark:text-white">
                I'm a 2021 First Class Honours Computer Science Graduate and Full-Stack Software Engineer.
                A life long interest in computers and academic experience in programming since Secondary School,
                I've learned a lot about programming principles, techniques and systems architecture. Through out
                the years I have developed a real passion for coding. Currently I am working on side projects,
                exploring technologies that are new to me and planning on contributing to Open Source software in the near future.
                I always love to have a laugh and discuss innovative ideas.
            </p>
          </div>
        </div>
      </div>

      <div class="py-10 border-t border-slate-200 dark:border-slate-500 text-justify">
        <div class="flex flex-wrap justify-center">
          <div class="w-full lg:w-9/12">
            <h2 class="mb-4 text-lg md:text-xl leading-relaxed text-slate-700 dark:text-white font-bold">
                EXPERIENCE
            </h2>
          </div>
          <div class="w-full lg:w-9/12">
            <p class="mb-4 md:text-lg leading-relaxed text-slate-700 dark:text-white">
              Full-Stack Engineer @ <a class="external-frontpage underline" href="https://www.equans.co.uk/" rel="noreferrer" target="_blank">Equans</a><br/>
              Software Consultant @ <a class="external-frontpage underline" href="https://www.netcompany.com" rel="noreferrer" target="_blank">Netcompany</a><br/>
              Junior Solution Engineer @ <a class="external-frontpage underline" href="https://www.crispthinking.com" rel="noreferrer" target="_blank">Crisp Thinking</a>
            </p>
          </div>
        </div>
      </div>

      <div class="py-10 border-t border-slate-200 dark:border-slate-500 text-justify">
        <div class="flex flex-wrap justify-center">
          <div class="w-full lg:w-9/12">
            <h2 class="mb-4 text-lg md:text-xl leading-relaxed text-slate-700 dark:text-white font-bold">
                EDUCATION
            </h2>
          </div>
          <div class="w-full lg:w-9/12">
            <p class="mb-4 md:text-lg leading-relaxed text-slate-700 dark:text-white">
              First Class Computer Science (BSc) @ <a class="external-frontpage underline" href="https://www.leedsbeckett.ac.uk/" rel="noreferrer" target="_blank">Leeds Beckett University</a><br/>
            </p>
          </div>
        </div>
      </div>


    </div>
  </div>
</div>
</section>