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

{#snippet slotBox(sponsor, sizeClass)}
	<a
		href={sponsor.url}
		target="_blank"
		rel="noopener noreferrer"
		aria-label={sponsor.name}
		class="sponsor-slot solar-clip-square flex items-center justify-center bg-[#EDD8BD] p-2 sm:p-3 lg:p-4 {sizeClass}"
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

<div class="relative w-full font-sweetsquare">
	<div
		class="pointer-events-none fixed inset-0 z-0 bg-navy bg-[url(/assets/sponsors-bg.png)] bg-cover bg-center"
	>
		<div class="absolute inset-0 bg-gradient-to-b from-black/45 via-navy/70 to-black/90"></div>
	</div>

	<!-- Hero -->
	<section class="relative z-10 flex h-screen w-full items-center justify-center px-6">
		<div class="flex max-w-5xl flex-col items-center text-center">
			<h1
				class="text-6xl font-black text-gold drop-shadow-logo sm:text-7xl lg:text-8xl xl:text-9xl"
			>
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
			<div class="mt-12 flex flex-col gap-5 sm:flex-row sm:gap-8">
				<a
					href="#"
					class="rounded-full bg-red px-10 py-4 text-xl font-black text-white transition-all hover:bg-white hover:text-navy sm:text-2xl lg:px-12 lg:text-3xl"
				>
					Become A Sponsor
				</a>
				<a
					href="#"
					class="rounded-full bg-red px-10 py-4 text-xl font-black text-white transition-all hover:bg-white hover:text-navy sm:text-2xl lg:px-12 lg:text-3xl"
				>
					Our Sponsor Packet
				</a>
			</div>
		</div>
	</section>

	<!-- Scarlet -->
	<section class="relative z-10 flex h-screen w-full flex-col items-center justify-center px-6 pt-16">
		<h2 class="text-6xl font-black text-red drop-shadow-logo sm:text-7xl lg:text-8xl xl:text-9xl">
			Scarlet
		</h2>
		<div class="mt-3 h-[3px] w-40 bg-red sm:w-56 lg:w-72"></div>
		<div class="mt-10 flex flex-col items-center gap-6 lg:mt-14 lg:gap-8">
			<div class="flex flex-wrap justify-center gap-5 lg:gap-8">
				{#each scarlet.slice(0, 3) as sponsor}
					{@render slotBox(sponsor, 'size-32 sm:size-44 lg:size-56')}
				{/each}
			</div>
			<div class="flex flex-wrap justify-center gap-5 lg:gap-8">
				{#each scarlet.slice(3) as sponsor}
					{@render slotBox(sponsor, 'size-32 sm:size-44 lg:size-56')}
				{/each}
			</div>
		</div>
	</section>

	<!-- Gold -->
	<section class="relative z-10 flex h-screen w-full flex-col items-center justify-center px-6 pt-16">
		<h2
			class="text-6xl font-black text-gold drop-shadow-[0_4px_0_#b07d12] sm:text-7xl lg:text-8xl xl:text-9xl"
		>
			Gold
		</h2>
		<div class="mt-3 h-[3px] w-32 bg-gold sm:w-44 lg:w-56"></div>
		<div class="mt-10 flex flex-col items-center gap-5 lg:mt-12 lg:gap-6">
			<div class="flex flex-wrap justify-center gap-5 lg:gap-6">
				{#each gold.slice(0, 3) as sponsor}
					{@render slotBox(sponsor, 'size-28 sm:size-36 lg:size-48')}
				{/each}
			</div>
			<div class="flex flex-wrap justify-center gap-5 lg:gap-6">
				{#each gold.slice(3) as sponsor}
					{@render slotBox(sponsor, 'size-28 sm:size-36 lg:size-48')}
				{/each}
			</div>
		</div>
	</section>

	<!-- Silver -->
	<section class="relative z-10 flex h-screen w-full flex-col items-center justify-center px-6 pt-16">
		<h2
			class="text-6xl font-black text-silver drop-shadow-logo sm:text-7xl lg:text-8xl xl:text-9xl"
		>
			Silver
		</h2>
		<div class="mt-3 h-[3px] w-36 bg-silver sm:w-52 lg:w-64"></div>
		<div class="mt-10 flex flex-col items-center gap-5 lg:mt-14 lg:gap-7">
			<div class="flex flex-wrap justify-center gap-4 lg:gap-5">
				{#each silver.slice(0, 4) as sponsor}
					{@render slotBox(sponsor, 'size-24 sm:size-32 lg:size-44')}
				{/each}
			</div>
			<div class="flex flex-wrap justify-center gap-4 lg:gap-5">
				{#each silver.slice(4) as sponsor}
					{@render slotBox(sponsor, 'size-24 sm:size-32 lg:size-44')}
				{/each}
			</div>
		</div>
	</section>

	<!-- Bronze -->
	<section class="relative z-10 flex h-screen w-full flex-col items-center justify-center px-6 pt-16">
		<h2 class="text-6xl font-black text-bronze drop-shadow-logo sm:text-7xl lg:text-8xl xl:text-9xl">
			Bronze
		</h2>
		<div class="mt-3 h-[3px] w-40 bg-bronze sm:w-56 lg:w-72"></div>
		<div class="mt-10 flex flex-col items-center gap-5 lg:mt-14 lg:gap-8">
			<div class="flex flex-wrap justify-center gap-5 lg:gap-8">
				{#each bronze.slice(0, 2) as sponsor}
					{@render slotBox(sponsor, 'size-32 sm:size-44 lg:size-56')}
				{/each}
			</div>
			<div class="flex flex-wrap justify-center gap-5 lg:gap-8">
				{#each bronze.slice(2) as sponsor}
					{@render slotBox(sponsor, 'size-32 sm:size-44 lg:size-56')}
				{/each}
			</div>
		</div>
	</section>
</div>

<style>
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
