<script lang="ts">
	import './layout.css';
	import Navlink from '$lib/navlink.svelte';
	const { children } = $props();

	let y = $state(0);
	let nav: Element;

	function onscroll() {
		if (y > 200) {
			nav.classList.add("nav-shadow");
		} else {
			nav.classList.remove("nav-shadow");
		}
	}

	$effect(()=>{
		onscroll();
	})

</script>

<svelte:window bind:scrollY={y} {onscroll} />

<div id="main-nav" bind:this={nav} class="transition-colors fixed z-100 w-full select-none justify-center align-middle flex pb-9 h-30 ">
	<nav class="z-100 select-none justify-between align-middle flex w-full max-w-content h-full">
		<a href="/" class="absolute pb-10 ml-5 flex-1 flex justify-center items-center h-full max-w-15">
			<img src="assets/solarlogo.svg" 
			alt="Rutgers Solar Car Icon">
		</a>
	
		<nav class="flex-1 justify-center flex">
			<Navlink label={"Team"} link={"/team"}></Navlink>
			<Navlink label={"Join"} link={"/join"}></Navlink>
			<Navlink label={"Sponsors"} link={"/sponsors"}></Navlink>
			<Navlink label={"Donate"} 
			link={"https://give.rutgersfoundation.org/rutgers-solar-car-team/20133.html"} 
			newtab={true}
			textclass={"text-gold"}
			></Navlink>
		</nav>
	</nav>
</div>


{@render children()}
