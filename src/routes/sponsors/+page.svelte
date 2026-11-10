<script>
	const logo = (page) => `/sponsors/sponsor-color-transparent/Page%20${page}.webp`;

	const scarlet = [
		{
			name: 'Badger Metal & Machine Fabrication, LLC',
			url: 'https://badgermetalfab.com',
			logo: logo(3)
		},
		{
			name: 'KOMO',
			url: 'https://komo.com',
			logo: logo(4)
		},
		{
			name: 'PMC (Polyurethane Machinery Corporation)',
			url: 'https://www.polymac-usa.com',
			logo: logo(5)
		},
		{
			name: 'Rutgers School of Engineering',
			url: 'https://soe.rutgers.edu',
			logo: logo(6)
		},
		{
			name: 'Viking Yachts',
			url: 'https://vikingyachts.com',
			logo: logo(7)
		}
	];

	const gold = [
		{
			name: 'General Sealants',
			url: 'https://generalsealants.com',
			logo: logo(16)
		},
		{
			name: "Mr. G's Workshop",
			url: 'https://rongrosinger.com',
			logo: logo(17)
		},
		{
			name: 'Panasonic',
			url: 'https://www.panasonic.com',
			logo: logo(18)
		},
		{
			name: 'Sunpower',
			url: 'https://us.sunpower.com',
			logo: logo(19)
		},
		{
			name: 'TeamGantt',
			url: 'https://www.teamgantt.com',
			logo: logo(20)
		},
		{
			name: 'Tri-Power Design',
			url: 'https://tripowerdesign.com',
			logo: logo(21)
		}
	];

	const silver = [
		{
			name: 'Airtech',
			url: 'https://www.airtech.com',
			logo: logo(9)
		},
		{
			name: 'Amolen',
			url: 'https://www.amolen.com',
			logo: logo(10)
		},
		{
			name: 'Bay Area Circuits',
			url: 'https://bayareacircuits.com',
			logo: logo(11)
		},
		{
			name: 'Endurans',
			url: 'https://endurans-solar.com',
			logo: logo(12)
		},
		{
			name: 'Lockheed Martin',
			url: 'https://lockheedmartin.com',
			logo: logo(13)
		},
		{
			name: 'PCBWay',
			url: 'https://www.pcbway.com',
			logo: logo(15)
		},
		{
			name: 'Rutgers Office of Climate Action',
			url: 'https://climateaction.rutgers.edu',
			logo: logo(14)
		},
		{
			name: 'Saint-Gobain',
			url: 'https://saint-gobain.com',
			logo: logo(8)
		}
	];

	const bronze = [
		{
			name: 'FSAEParts',
			url: 'https://fsaeparts.com',
			logo: logo(22)
		},
		{
			name: 'Hawkeye Industries',
			url: 'https://hawkeyeind.com',
			logo: '/sponsors/sponsor-color-transparent/hawkeye.png'
		},
		{
			name: 'Tilton Engineering FSAE',
			url: 'https://www.tiltonracing.com',
			logo: '/sponsors/sponsor-color-transparent/tilton.png'
		},
		{
			name: 'Wilwood Engineering',
			url: 'https://www.wilwood.com',
			logo: '/sponsors/sponsor-color-transparent/wilwood.png'
		}
	];
</script>

{#snippet slotBox(sponsor)}
	<a
		href={sponsor.url}
		target="_blank"
		rel="noopener noreferrer"
		aria-label={sponsor.name}
		class="sponsor-slot solar-clip-square flex aspect-square w-full items-center justify-center bg-[#EDD8BD] p-2 sm:p-3 lg:p-4"
	>
		{#if sponsor.logo}
			<img src={sponsor.logo} alt="" class="h-full w-full object-contain" />
		{:else}
			<span class="px-2 text-center text-sm font-black leading-tight text-navy sm:text-base lg:text-lg">
				{sponsor.name}
			</span>
		{/if}
	</a>
{/snippet}

{#snippet sponsorGrid(list, widthClass, layout)}
	<div
		class="mx-auto grid gap-3 sm:gap-5 {widthClass} {layout === 'row' ? 'grid-cols-4' : 'grid-cols-6'}"
	>
		{#each list as sponsor, i}
			{@const centerPair =
				layout === 'pairs' ? i % 2 === 0 : layout === 'rows' && i % 3 === 0 && list.length - i === 2}
			<div class="min-w-0 {layout === 'row' ? '' : 'col-span-2'} {centerPair ? 'col-start-2' : ''}">
				{@render slotBox(sponsor)}
			</div>
		{/each}
	</div>
{/snippet}

<div class="relative w-full font-sweetsquare">
	<div
		class="pointer-events-none fixed inset-0 z-0 bg-navy bg-[url(/assets/sponsors-bg.png)] bg-cover bg-center"
	>
		<div class="absolute inset-0 bg-gradient-to-b from-black/45 via-navy/70 to-black/90"></div>
	</div>

	<!-- Hero -->
	<section class="relative z-10 flex h-screen w-full items-center justify-center px-6">
		<div class="flex max-w-5xl flex-col items-center text-center">
			<h1 class="text-6xl font-black text-gold sm:text-7xl lg:text-8xl xl:text-9xl">
				Sponsors
			</h1>
			<div class="mt-4 h-[3px] w-48 bg-red sm:w-64 lg:w-80"></div>
			<p
				class="mt-8 max-w-3xl text-lg font-bold text-white drop-shadow-small sm:text-2xl lg:text-3xl"
			>
				Rutgers Solar Car would not exist without your help! We appreciate any and
				all donations.
			</p>
			<p
				class="mt-8 max-w-3xl text-lg font-bold text-white drop-shadow-small sm:text-2xl lg:text-3xl"
			>
				If you're interested in becoming one of our sponsors, please contact us
				through our email or social media platforms!
			</p>
			<a
				href="mailto:rusolarcarclub@gmail.com"
				class="sponsor-cta mt-12 inline-block bg-red px-14 py-4 text-xl font-black text-white transition-all hover:bg-white hover:text-navy sm:text-2xl lg:text-3xl"
			>
				Become A Sponsor
			</a>
		</div>
	</section>

	<!-- Scarlet -->
	<section class="tier">
		<h2 class="text-6xl font-black text-red sm:text-7xl lg:text-8xl xl:text-9xl">Scarlet</h2>
		<div class="mt-3 h-[3px] w-40 bg-red sm:w-56 lg:w-72"></div>
		<div class="mt-8 w-full">
			{@render sponsorGrid(scarlet, 'w-[104%] max-w-[48rem]', 'rows')}
		</div>
	</section>

	<!-- Gold -->
	<section class="tier">
		<h2 class="text-6xl font-black text-gold sm:text-7xl lg:text-8xl xl:text-9xl">Gold</h2>
		<div class="mt-3 h-[3px] w-32 bg-gold sm:w-44 lg:w-56"></div>
		<div class="mt-8 w-full">
			{@render sponsorGrid(gold, 'w-[90%] max-w-[42rem]', 'rows')}
		</div>
	</section>

	<!-- Silver -->
	<section class="tier">
		<h2 class="text-6xl font-black text-silver sm:text-7xl lg:text-8xl xl:text-9xl">Silver</h2>
		<div class="mt-3 h-[3px] w-36 bg-silver sm:w-52 lg:w-64"></div>
		<div class="mt-8 w-full">
			{@render sponsorGrid(silver, 'w-[83%] max-w-[37.5rem]', 'rows')}
		</div>
	</section>

	<!-- Bronze -->
	<section class="tier">
		<h2 class="text-6xl font-black text-bronze sm:text-7xl lg:text-8xl xl:text-9xl">Bronze</h2>
		<div class="mt-3 h-[3px] w-40 bg-bronze sm:w-56 lg:w-72"></div>
		<div class="mt-8 w-full">
			{@render sponsorGrid(bronze, 'w-full max-w-[46rem]', 'row')}
		</div>
	</section>
</div>

<style>
	.tier {
		position: relative;
		z-index: 10;
		display: flex;
		width: 100%;
		flex-direction: column;
		align-items: center;
		padding: 3rem 1rem;
	}

	.sponsor-cta {
		clip-path: polygon(
			1rem 0,
			calc(100% - 1rem) 0,
			100% 1rem,
			100% calc(100% - 1rem),
			calc(100% - 1rem) 100%,
			1rem 100%,
			0 calc(100% - 1rem),
			0 1rem
		);
		filter: drop-shadow(-4px 4px 0 var(--color-shadow));
	}

	.sponsor-cta:hover {
		filter: drop-shadow(-4px 8px 0 var(--color-shadow));
	}

	.sponsor-slot {
		position: relative;
		overflow: hidden;
		cursor: pointer;
		filter: drop-shadow(-4px 4px 0 var(--color-shadow));
		transition:
			transform 0.4s var(--ease-frame),
			filter 0.4s ease;
	}

	.sponsor-slot:hover {
		transform: scale(1.08) translateY(-6px);
		filter: drop-shadow(-4px 8px 0 var(--color-shadow));
	}

	.sponsor-slot::after {
		content: '';
		position: absolute;
		inset: 0;
		background: linear-gradient(
			120deg,
			transparent 30%,
			rgba(255, 255, 255, 0.22) 50%,
			transparent 70%
		);
		transform: translateX(-130%);
		pointer-events: none;
	}

	.sponsor-slot:hover::after {
		animation: slot-shine 0.55s ease-out;
	}

	@keyframes slot-shine {
		to {
			transform: translateX(130%);
		}
	}
</style>
