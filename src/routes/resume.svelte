<script>
  import Alink from '$lib/alink.svelte';
  import { onMount } from 'svelte';

	let StackOverFlowCount = '-1';
  let reposCount = '...'
	
	function handleMouseOver() {
		StackOverFlowCount = '😉';
	}
	function handleMouseOut() {
		StackOverFlowCount = '-1';
	}

  async function fetchReposCount() {
    const repos = await fetch(`https://api.github.com/users/Beenyaa/repos`).then(r => r.json());
    reposCount = repos.length
}

	onMount(fetchReposCount);
</script>

<section class="pt-16">
<div class="container lg:w-10/12 px-4 mx-auto mb-10">
  <div class="relative flex flex-col min-w-0 break-words bg-white/[.62] dark:bg-slate-800/[.62] backdrop-filter backdrop-blur-xl w-full mb-6 dark:shadow-slate-800 shadow-xl rounded-lg mb-16">
    <div class="px-6">
      <div class="flex flex-wrap justify-center">
        <div class="w-full flex justify-center">
          <div class="mb-12">
            <img alt="..." src="/me.webp" class="mask mask-squircle h-36 w-36 mx-auto align-middle border-none absolute -m-16 -ml-20 lg:-ml-16">
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
          <div class="w-full px-4 text-center">
            <div class="flex justify-center py-4 lg:pt-4 pt-8">
              <a href="https://github.com/Beenyaa" rel="noreferrer" target="_blank" class="p-3 text-center">
                <svg class="w-10 h-10 fill-slate-700 dark:fill-gray-200 hover:dark:fill-white hover:fill-black" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 496 512"><!--! Font Awesome Pro 6.1.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. --><path d="M165.9 397.4c0 2-2.3 3.6-5.2 3.6-3.3.3-5.6-1.3-5.6-3.6 0-2 2.3-3.6 5.2-3.6 3-.3 5.6 1.3 5.6 3.6zm-31.1-4.5c-.7 2 1.3 4.3 4.3 4.9 2.6 1 5.6 0 6.2-2s-1.3-4.3-4.3-5.2c-2.6-.7-5.5.3-6.2 2.3zm44.2-1.7c-2.9.7-4.9 2.6-4.6 4.9.3 2 2.9 3.3 5.9 2.6 2.9-.7 4.9-2.6 4.6-4.6-.3-1.9-3-3.2-5.9-2.9zM244.8 8C106.1 8 0 113.3 0 252c0 110.9 69.8 205.8 169.5 239.2 12.8 2.3 17.3-5.6 17.3-12.1 0-6.2-.3-40.4-.3-61.4 0 0-70 15-84.7-29.8 0 0-11.4-29.1-27.8-36.6 0 0-22.9-15.7 1.6-15.4 0 0 24.9 2 38.6 25.8 21.9 38.6 58.6 27.5 72.9 20.9 2.3-16 8.8-27.1 16-33.7-55.9-6.2-112.3-14.3-112.3-110.5 0-27.5 7.6-41.3 23.6-58.9-2.6-6.5-11.1-33.3 2.6-67.9 20.9-6.5 69 27 69 27 20-5.6 41.5-8.5 62.8-8.5s42.8 2.9 62.8 8.5c0 0 48.1-33.6 69-27 13.7 34.7 5.2 61.4 2.6 67.9 16 17.7 25.8 31.5 25.8 58.9 0 96.5-58.9 104.2-114.8 110.5 9.2 7.9 17 22.9 17 46.4 0 33.7-.3 75.4-.3 83.6 0 6.5 4.6 14.4 17.3 12.1C428.2 457.8 496 362.9 496 252 496 113.3 383.5 8 244.8 8zM97.2 352.9c-1.3 1-1 3.3.7 5.2 1.6 1.6 3.9 2.3 5.2 1 1.3-1 1-3.3-.7-5.2-1.6-1.6-3.9-2.3-5.2-1zm-10.8-8.1c-.7 1.3.3 2.9 2.3 3.9 1.6 1 3.6.7 4.3-.7.7-1.3-.3-2.9-2.3-3.9-2-.6-3.6-.3-4.3.7zm32.4 35.6c-1.6 1.3-1 4.3 1.3 6.2 2.3 2.3 5.2 2.6 6.5 1 1.3-1.3.7-4.3-1.3-6.2-2.2-2.3-5.2-2.6-6.5-1zm-11.4-14.7c-1.6 1-1.6 3.6 0 5.9 1.6 2.3 4.3 3.3 5.6 2.3 1.6-1.3 1.6-3.9 0-6.2-1.4-2.3-4-3.3-5.6-2z"/></svg>
              </a>
              <a href="https://linkedin.com/in/bencepdf" rel="noreferrer" target="_blank" class="p-3 text-center">
                <svg class="w-10 h-10 fill-slate-700 dark:fill-gray-200 hover:dark:fill-white hover:fill-black" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"><!--! Font Awesome Pro 6.1.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. --><path d="M416 32H31.9C14.3 32 0 46.5 0 64.3v383.4C0 465.5 14.3 480 31.9 480H416c17.6 0 32-14.5 32-32.3V64.3c0-17.8-14.4-32.3-32-32.3zM135.4 416H69V202.2h66.5V416zm-33.2-243c-21.3 0-38.5-17.3-38.5-38.5S80.9 96 102.2 96c21.2 0 38.5 17.3 38.5 38.5 0 21.3-17.2 38.5-38.5 38.5zm282.1 243h-66.4V312c0-24.8-.5-56.7-34.5-56.7-34.6 0-39.9 27-39.9 54.9V416h-66.4V202.2h63.7v29.2h.9c8.9-16.8 30.6-34.5 62.9-34.5 67.2 0 79.7 44.3 79.7 101.9V416z"/></svg>
              </a>
              <a href="https://instagram.com/bence.jpeg" rel="noreferrer" target="_blank" class="p-3 text-center">
                <svg class="w-10 h-10 fill-slate-700 dark:fill-gray-200 hover:dark:fill-white hover:fill-black" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"><!--! Font Awesome Pro 6.1.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. --><path d="M224.1 141c-63.6 0-114.9 51.3-114.9 114.9s51.3 114.9 114.9 114.9S339 319.5 339 255.9 287.7 141 224.1 141zm0 189.6c-41.1 0-74.7-33.5-74.7-74.7s33.5-74.7 74.7-74.7 74.7 33.5 74.7 74.7-33.6 74.7-74.7 74.7zm146.4-194.3c0 14.9-12 26.8-26.8 26.8-14.9 0-26.8-12-26.8-26.8s12-26.8 26.8-26.8 26.8 12 26.8 26.8zm76.1 27.2c-1.7-35.9-9.9-67.7-36.2-93.9-26.2-26.2-58-34.4-93.9-36.2-37-2.1-147.9-2.1-184.9 0-35.8 1.7-67.6 9.9-93.9 36.1s-34.4 58-36.2 93.9c-2.1 37-2.1 147.9 0 184.9 1.7 35.9 9.9 67.7 36.2 93.9s58 34.4 93.9 36.2c37 2.1 147.9 2.1 184.9 0 35.9-1.7 67.7-9.9 93.9-36.2 26.2-26.2 34.4-58 36.2-93.9 2.1-37 2.1-147.8 0-184.8zM398.8 388c-7.8 19.6-22.9 34.7-42.6 42.6-29.5 11.7-99.5 9-132.1 9s-102.7 2.6-132.1-9c-19.6-7.8-34.7-22.9-42.6-42.6-11.7-29.5-9-99.5-9-132.1s-2.6-102.7 9-132.1c7.8-19.6 22.9-34.7 42.6-42.6 29.5-11.7 99.5-9 132.1-9s102.7-2.6 132.1 9c19.6 7.8 34.7 22.9 42.6 42.6 11.7 29.5 9 99.5 9 132.1s2.7 102.7-9 132.1z"/></svg>
              </a>
              <a href="https://twitter.com/bencetxt" rel="noreferrer" target="_blank" class="p-3 text-center">
                <svg class="w-10 h-10 fill-slate-700 dark:fill-gray-200 hover:dark:fill-white hover:fill-black" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512"><!--! Font Awesome Pro 6.1.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. --><path d="M459.37 151.716c.325 4.548.325 9.097.325 13.645 0 138.72-105.583 298.558-298.558 298.558-59.452 0-114.68-17.219-161.137-47.106 8.447.974 16.568 1.299 25.34 1.299 49.055 0 94.213-16.568 130.274-44.832-46.132-.975-84.792-31.188-98.112-72.772 6.498.974 12.995 1.624 19.818 1.624 9.421 0 18.843-1.3 27.614-3.573-48.081-9.747-84.143-51.98-84.143-102.985v-1.299c13.969 7.797 30.214 12.67 47.431 13.319-28.264-18.843-46.781-51.005-46.781-87.391 0-19.492 5.197-37.36 14.294-52.954 51.655 63.675 129.3 105.258 216.365 109.807-1.624-7.797-2.599-15.918-2.599-24.04 0-57.828 46.782-104.934 104.934-104.934 30.213 0 57.502 12.67 76.67 33.137 23.715-4.548 46.456-13.32 66.599-25.34-7.798 24.366-24.366 44.833-46.132 57.827 21.117-2.273 41.584-8.122 60.426-16.243-14.292 20.791-32.161 39.308-52.628 54.253z"/></svg>
              </a>
              <a href="mailto:hey@bence.codes" rel="noreferrer" target="_blank" class="p-3 text-center">
                <svg class="w-10 h-10 fill-slate-700 dark:fill-gray-200 hover:dark:fill-white hover:fill-black" viewBox="0 0 512 512"><!--! Font Awesome Pro 6.1.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. --><path d="M464 64C490.5 64 512 85.49 512 112C512 127.1 504.9 141.3 492.8 150.4L275.2 313.6C263.8 322.1 248.2 322.1 236.8 313.6L19.2 150.4C7.113 141.3 0 127.1 0 112C0 85.49 21.49 64 48 64H464zM217.6 339.2C240.4 356.3 271.6 356.3 294.4 339.2L512 176V384C512 419.3 483.3 448 448 448H64C28.65 448 0 419.3 0 384V176L217.6 339.2z"/></svg>
              </a>
            </div>
          </div>
          <div class="mb-2 text-slate-600 dark:text-white">
            <i class="fas fa-briefcase mr-2 text-lg text-slate-400"></i>
            <Alink link={"https://www.equans.co.uk"} text={"Full-Stack Engineer @ Equans"}/>
          </div>
          <div class="mb-2 text-slate-600 dark:text-white">
            First Class Computer Science (BSc)
          </div>
        </div>
        <div class="w-full px-4 text-center">
          <div class="flex justify-center py-4 lg:pt-4 pt-8">
            <!-- <div class="mr-4 p-3 text-center">
              <span class="text-xl font-bold block uppercase tracking-wide text-slate-600 dark:text-white">
                0
              </span>
              <span class="text-sm text-slate-400">Projects</span>
            </div> -->
            <div class="mr-4 p-3 text-center">
              <span class="text-xl font-bold block uppercase tracking-wide text-slate-600 dark:text-white dark:text-white">
                {reposCount}
              </span>
              <span class="text-sm text-slate-400">Github <br/>Public Repos</span>
            </div>
            <div class="lg:mr-4 p-3 text-center" on:mouseover={handleMouseOver} on:click={handleMouseOver} on:mouseout={handleMouseOut}>
              <span class="text-xl font-bold block uppercase tracking-wide text-slate-600 dark:text-white">
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
          <table class="table-auto lg:w-9/12">
            <thead>
              <tr>
                <th hidden class="text-left">experience</th>
              </tr>
            </thead>
          
            <tbody class="mb-4 md:text-lg leading-relaxed text-slate-700 dark:text-white">
              <tr>
                <td class="text-left"> <b>2022 - PRESENT
                 Full-Stack Engineer
                  <Alink link={"https://www.equans.co.uk"} text={"Equans"}/></b>
                </td>
              </tr>
              <tr>
                <td>
                  Smart Buildings Department, working with Nest.js, TypeScript and React.
                </td>
              </tr>
              <tr>
                <td class="text-left"> <b>2021 - 2022
                  Software Consultant
                  <Alink link={"https://www.netcompany.com"} text={"Netcompany"}/></b>
                </td>
              </tr>
              <tr>
                <td>
                  Consultancy work with public and private sector clients. Used Angular12, TypeScript, Java 11, Spring and Cucumber.
                </td>
              </tr>
              <tr>
                <td class="text-left"> 
                  <b>2019 - 2021
                  Junior Solution Engineer
                  <Alink link={"https://www.crispthinking.com"} text={"Crisp Thinking"}/></b>
                </td>
              </tr>
              <tr>
                <td> A lot of data collation, data cleaning and fun Proof Of Concepting with Python and JavaScript.</td>
              </tr>
            </tbody>
          </table>
        </div>
      </div>

      <div class="py-10 border-t border-slate-200 dark:border-slate-500 text-justify">
        <div class="flex flex-wrap justify-center">
          <div class="w-full lg:w-9/12">
            <h2 class="mb-4 text-lg md:text-xl leading-relaxed text-slate-700 dark:text-white font-bold">
                EDUCATION
            </h2>
          </div>
          <table class="table-auto lg:w-9/12">
            <thead>
              <tr>
                <th hidden class="text-left">experience</th>
              </tr>
            </thead>
          
            <tbody class="mb-4 md:text-lg leading-relaxed text-slate-700 dark:text-white">
              <tr>
                <td class="text-left"> <b>2018 - 2021
                  First Class Computer Science (BSc)
                  <Alink link={"https://www.leedsbeckett.ac.uk"} text={"Leeds Beckett University"}/>
                </td>
              </tr>
              <tr>
                <td>
                  During my time at University, I have completed modules involving developing and querying SQL Databases in Oracle and developing a variety 
                  of applications in Java and C# .NET in an Object Orientated way for desktop, mobile and web applications. I have also been made familiar
                   with the Linux/Unix Operating Systems and their command line tools.
                </td>
              </tr>
            </tbody>
          </table>
        </div>
      </div>


    </div>
  </div>
</div>
</section>

<style>
  .mask{
    -webkit-mask-size: contain;
    mask-size: contain;
    -webkit-mask-repeat: no-repeat;
    mask-repeat: no-repeat;
    -webkit-mask-position: center;
    mask-position: center;
  }
  .mask-squircle{
    -webkit-mask-image: url(/squircle.svg);
    mask-image: url(/squircle.svg);
  }
  </style>