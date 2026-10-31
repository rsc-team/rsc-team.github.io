<!-----
Navigation bar
------->

<script lang="ts">
	import './layout.css';
	import Navlink from '$lib/navlink.svelte';
	const { children } = $props();

	let y = $state(0);
	let nav: Element;
	let navbuttons:Element;

	let naventrance:Element;
	let naventranceinner:Element;

	let burgermode = false

	let burgerclass = "flex flex-col items-center bg-navy-opaque w-full h-full scale-150 fixed top-1/2 left-1/2 -translate-y-1/2 -translate-x-1/2"

	function onscroll() {
		if (y > 200) {
			nav.classList.add("nav-shadow");
		} else {
			nav.classList.remove("nav-shadow");
		}
	}

	let cancelMenuTargets = ["naventrance","navmenu","rscicon"]

	function clickedwindow(e:PointerEvent) {
		if (e.target != null) {
			let target : Element = e.target as Element
			if ((cancelMenuTargets.includes(target.id) || target.classList.contains("navigation-button")) && burgermode) { 
				hamburger() 
			}
		}
	}

	function hamburger() {
		burgermode = !burgermode

		if (burgermode) {
			burgerclass.split(" ").forEach((c)=>{navbuttons.classList.add(c)})
			naventrance.classList.toggle("bg-red")
			naventranceinner.classList.toggle("bg-navy")
			naventranceinner.classList.toggle("bg-red")
			navbuttons.classList.remove("hidden")
		} else {
			burgerclass.split(" ").forEach((c)=>{navbuttons.classList.remove(c)})
			naventrance.classList.toggle("bg-red")
			naventranceinner.classList.toggle("bg-navy")
			naventranceinner.classList.toggle("bg-red")
			navbuttons.classList.add("hidden")
		}
	}

	$effect(()=>{
		onscroll();
	})

</script>

<svelte:window bind:scrollY={y} {onscroll} onclick={clickedwindow} />

<div id="main-nav" bind:this={nav} class="transition-colors fixed z-100 w-full select-none justify-center align-middle flex h-20 ">
	<nav class="z-100 select-none justify-between align-middle flex w-full max-w-content h-full">
		<a href="/" class="absolute ml-5 flex-1 flex justify-center items-center h-full max-w-15">
			<img class="transition-all opacity-80 hover:opacity-100" src="/assets/solarlogo.svg" 
			alt="Rutgers Solar Car Icon">
		</a>
	
		<nav id="navmenu" bind:this={navbuttons} class="transition-all hidden sm:flex flex-1 m-auto align-middle content-center justify-center">
			<Navlink label={"Team"} link={"/team"}></Navlink>
			<!--<Navlink label={"Join"} link={"/join"}></Navlink>-->
			<Navlink label={"Sponsors"} link={"/sponsors"}></Navlink>
			<Navlink label={"Donate"} 
			link={"https://give.rutgersfoundation.org/rutgers-solar-car-team/20133.html"} 
			newtab={true}
			></Navlink>
			
		</nav>
		<button bind:this={naventrance} onclick={hamburger}  class=" sm:hidden group m-auto h-12 w-12 p-2 transition-all cursor-pointer mr-5 hover:bg-red solar-clip-square">
			<div id="navbutton" bind:this={naventranceinner} class="transition-all h-full w-full mask-contain mask-[url(/icons/menu-small.svg)] group-hover:bg-navy  bg-red"></div>
		</button>
	</nav>
</div>


{@render children()}
