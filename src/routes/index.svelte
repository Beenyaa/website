<script>
    import Alink from '$lib/alink.svelte';
</script>

<div class="flex relative flex-col justify-center items-center">
    <div class="container mx-auto px-6 flex flex-col justify-between items-center relative py-4 mt-16 md:mt-10">
        <div class="flex flex-col">
            <img src="/bence-face.webp" class="mask mask-squircle h-36 w-36 mx-auto" alt=""/>
            <h1 class="md:mt-10 max-w-2xl text-3xl md:text-5xl font-bold mx-auto dark:text-white text-gray-800 text-center py-2">
                <span class="wave">👋</span> Hey, Internet!
            </h1>
            <p class="max-w-2xl text-lg md:text-2xl my-6 text-left dark:text-white" >
                I&#x27;m Bence, a Hungarian guy based in the UK and 
                <Alink link={"https://www.equans.co.uk/"} text={"Full-Stack Engineer @ Equans"}/>, 
                currently experimenting with emerging and evolving technologies.
            </p>
            <div class="flex items-center justify-center">
                <a href="/resume" class="uppercase py-2 my-2 px-4 md:mt-10 bg-transparent border-2 dark:border-gray-100 ease-in duration-200 dark:text-white hover:dark:bg-gray-100 hover:dark:text-gray-800 border-gray-800 text-gray-800 hover:bg-gray-800 hover:text-white text-md">
                    CONNECT WITH ME
                </a>
            </div>
        </div>
    </div>
</div>

<style>
    .wave {
    -webkit-animation-name: wave-animation;
    animation-name: wave-animation;
    -webkit-animation-duration: 2.5s;
    animation-duration: 2.5s;
    -webkit-animation-iteration-count: infinite;
    animation-iteration-count: infinite;
    transform-origin: 70% 70%;
    display: inline-block;
}

@-webkit-keyframes wave-animation {
    0% {
     transform:rotate(0deg)
    }
    10% {
     transform:rotate(14deg)
    }
    20% {
     transform:rotate(-8deg)
    }
    30% {
     transform:rotate(14deg)
    }
    40% {
     transform:rotate(-4deg)
    }
    50% {
     transform:rotate(10deg)
    }
    60% {
     transform:rotate(0deg)
    }
    100% {
     transform:rotate(0deg)
    }
   }
   @keyframes wave-animation {
    0% {
     transform:rotate(0deg)
    }
    10% {
     transform:rotate(14deg)
    }
    20% {
     transform:rotate(-8deg)
    }
    30% {
     transform:rotate(14deg)
    }
    40% {
     transform:rotate(-4deg)
    }
    50% {
     transform:rotate(10deg)
    }
    60% {
     transform:rotate(0deg)
    }
    100% {
     transform:rotate(0deg)
    }
   }
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