<script lang="ts">
	import { base } from '$app/paths';

	const phone = '210-970-6829';
	const phoneHref = 'tel:+12109706829';
	const email = 'raeleen.cleaningco@gmail.com';
	const emailHref = `mailto:${email}`;

	type Service = { title: string; description: string; icon: string };

	const services: Service[] = [
		{
			title: 'Standard Residential',
			description: 'Routine refresh cleanings to keep your home sparkling week after week.',
			icon: 'home'
		},
		{
			title: 'Deep Cleaning',
			description: 'Top-to-bottom detail work for the spaces that everyday cleans can miss.',
			icon: 'sparkles'
		},
		{
			title: 'Move-In / Move-Out',
			description: 'Leave your old place spotless, or step into your new one feeling fresh.',
			icon: 'truck'
		},
		{
			title: 'Airbnb & Short-Term Turnovers',
			description: 'Fast, reliable turnovers that keep your guests reviewing 5 stars.',
			icon: 'key'
		},
		{
			title: 'Studio & Creative Spaces',
			description: 'A clean, calm studio so you can focus on the work that matters.',
			icon: 'palette'
		},
		{
			title: 'Office & Commercial',
			description: 'Consistent, professional cleaning for offices and small businesses.',
			icon: 'building'
		},
		{
			title: 'Post-Construction Cleanup',
			description: 'Dust, debris, and grime cleared so you can enjoy the finished space.',
			icon: 'hammer'
		},
		{
			title: 'Same-Day / Emergency',
			description: 'Last-minute clean? We help when we can — just give us a call.',
			icon: 'clock'
		}
	];

	const pricing = [
		{ label: 'Homes under 1,000 sq ft', price: '$120+' },
		{ label: 'Homes 1,000 – 2,000 sq ft', price: '$180+' },
		{ label: 'Homes 2,000+ sq ft', price: 'Custom Quote' },
		{ label: 'Airbnb Turnovers', price: '$100+' },
		{ label: 'Commercial & Studio Spaces', price: 'Custom Pricing' }
	];

	const addOns = [
		'Inside Oven Cleaning',
		'Inside Refrigerator Cleaning',
		'Baseboards & Detail Cleaning',
		'Interior Window Cleaning',
		'Laundry Services',
		'Dishwashing',
		'Organization & Home Reset',
		'Linen Changes & Airbnb Restocking',
		'Pet Hair Removal',
		'Trash Removal',
		'Eco-Friendly Cleaning Options'
	];

	const pestServices = [
		'Ant Control',
		'Roach Treatment',
		'Spider Prevention',
		'General Pest Prevention'
	];

	const reasons = [
		{
			title: 'Reliable & Professional Team',
			description: 'Show up when we say we will and leave your space looking its best.'
		},
		{
			title: 'Detail-Oriented Luxury Style',
			description: 'The small things matter — baseboards, corners, behind the appliances.'
		},
		{
			title: 'Flexible Scheduling',
			description: 'One-time, weekly, biweekly, monthly, or short-notice — we work around you.'
		},
		{
			title: 'Great for Families, Hosts & Businesses',
			description: 'Homes, Airbnbs, studios, and offices — each gets the care it deserves.'
		},
		{
			title: 'Judgment-Free Cleaning',
			description: "However the space looks today is fine. We're here to help."
		},
		{
			title: 'Consistent Communication & Care',
			description: 'Clear scheduling, clear pricing, and clear updates every step of the way.'
		}
	];

	const navLinks = [
		{ href: '#services', label: 'Services' },
		{ href: '#pricing', label: 'Pricing' },
		{ href: '#pest', label: 'Pest Control' },
		{ href: '#area', label: 'Service Area' },
		{ href: '#about', label: 'About' },
		{ href: '#contact', label: 'Contact' }
	];
</script>

<div class="bg-white text-brand-950">
	<!-- Top Nav -->
	<header class="sticky top-0 z-30 border-b border-brand-100 bg-white/85 backdrop-blur">
		<nav class="mx-auto flex max-w-6xl items-center justify-between px-5 py-4">
			<a href="#top" class="flex items-baseline gap-2">
				<span class="font-display text-2xl leading-none tracking-wide text-brand-700">Raeleen</span>
				<span class="font-display text-xl leading-none text-brand-500">Cleaning Co.</span>
			</a>
			<ul class="hidden items-center gap-7 text-sm font-semibold text-brand-900 md:flex">
				{#each navLinks as link (link.href)}
					<li>
						<a class="transition hover:text-brand-600" href={link.href}>{link.label}</a>
					</li>
				{/each}
			</ul>
			<a
				href={phoneHref}
				class="hidden rounded-full bg-brand-300 px-5 py-2 text-sm font-bold text-brand-950 shadow-sm transition hover:bg-brand-400 sm:inline-flex"
			>
				Call {phone}
			</a>
		</nav>
	</header>

	<!-- Hero -->
	<section
		id="top"
		class="relative overflow-hidden bg-gradient-to-b from-brand-100 via-brand-50 to-white"
	>
		<div
			class="pointer-events-none absolute -top-32 -right-32 h-96 w-96 rounded-full bg-brand-300/40 blur-3xl"
		></div>
		<div
			class="pointer-events-none absolute -bottom-40 -left-32 h-96 w-96 rounded-full bg-brand-200/60 blur-3xl"
		></div>

		<div
			class="relative mx-auto grid max-w-6xl items-center gap-12 px-5 py-20 md:grid-cols-2 md:py-28"
		>
			<div>
				<span
					class="inline-flex items-center gap-2 rounded-full bg-white px-3 py-1 text-xs font-bold tracking-wider text-brand-700 uppercase shadow-sm ring-1 ring-brand-200"
				>
					<span class="h-2 w-2 rounded-full bg-brand-500"></span>
					Serving Greater San Antonio
				</span>
				<h1 class="mt-5 font-display text-5xl leading-[1.05] text-brand-900 md:text-7xl">
					A spotless home.
					<span class="block text-brand-500">A peaceful space.</span>
				</h1>
				<p class="mt-6 max-w-xl text-lg text-brand-900/80 md:text-xl">
					Reliable, detail-focused residential and commercial cleaning across San Antonio, Texas.
					Homes, Airbnbs, studios, and offices — left fresh, welcoming, and guest-ready.
				</p>
				<div class="mt-8 flex flex-wrap gap-3">
					<a
						href={phoneHref}
						class="inline-flex items-center gap-2 rounded-full bg-brand-500 px-6 py-3 font-bold text-white shadow-md transition hover:bg-brand-600"
					>
						<svg
							class="h-5 w-5"
							viewBox="0 0 24 24"
							fill="none"
							stroke="currentColor"
							stroke-width="2"
							stroke-linecap="round"
							stroke-linejoin="round"
						>
							<path
								d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07 19.5 19.5 0 0 1-6-6 19.79 19.79 0 0 1-3.07-8.67A2 2 0 0 1 4.11 2h3a2 2 0 0 1 2 1.72c.13.96.37 1.9.72 2.81a2 2 0 0 1-.45 2.11L8.09 9.91a16 16 0 0 0 6 6l1.27-1.27a2 2 0 0 1 2.11-.45c.91.35 1.85.59 2.81.72A2 2 0 0 1 22 16.92z"
							/>
						</svg>
						{phone}
					</a>
					<a
						href={emailHref}
						class="inline-flex items-center gap-2 rounded-full bg-white px-6 py-3 font-bold text-brand-700 shadow-md ring-1 ring-brand-200 transition hover:bg-brand-50"
					>
						<svg
							class="h-5 w-5"
							viewBox="0 0 24 24"
							fill="none"
							stroke="currentColor"
							stroke-width="2"
							stroke-linecap="round"
							stroke-linejoin="round"
						>
							<rect x="3" y="5" width="18" height="14" rx="2" />
							<path d="m3 7 9 6 9-6" />
						</svg>
						Email Raeleen
					</a>
				</div>

				<div class="mt-10 grid grid-cols-3 gap-6 text-center md:max-w-md md:text-left">
					{#each [{ k: 'Trusted', v: 'Owner-operated' }, { k: 'Local', v: 'Inside Loop 410' }, { k: 'Flexible', v: 'Custom quotes' }] as stat (stat.k)}
						<div>
							<p class="font-display text-2xl text-brand-700">{stat.k}</p>
							<p class="text-sm text-brand-900/70">{stat.v}</p>
						</div>
					{/each}
				</div>
			</div>

			<div class="relative">
				<div
					class="absolute -inset-6 rounded-[2.5rem] bg-gradient-to-br from-brand-300 to-brand-500 opacity-50 blur-2xl"
				></div>
				<div
					class="relative overflow-hidden rounded-[2rem] bg-white shadow-2xl ring-1 ring-brand-100"
				>
					<img
						src="{base}/raeleen.jpg"
						alt="Raeleen Torres, owner of Raeleen Cleaning Co."
						class="aspect-[4/5] w-full object-cover"
					/>
					<div class="absolute right-4 bottom-4 rounded-2xl bg-white/95 px-4 py-3 shadow-lg">
						<p class="font-display text-lg leading-none text-brand-700">Raeleen Torres</p>
						<p class="text-xs font-semibold text-brand-900/70">Owner & Operator</p>
					</div>
				</div>
			</div>
		</div>
	</section>

	<!-- Services -->
	<section id="services" class="mx-auto max-w-6xl scroll-mt-24 px-5 py-20 md:py-28">
		<div class="max-w-2xl">
			<p class="text-sm font-bold tracking-widest text-brand-500 uppercase">What we do</p>
			<h2 class="mt-2 font-display text-4xl text-brand-900 md:text-5xl">Our Cleaning Services</h2>
			<p class="mt-4 text-lg text-brand-900/80">
				Whether you need a routine refresh, a deep clean, a move-in / move-out service, or an Airbnb
				turnover — our team makes your space feel spotless, peaceful, and guest-ready.
			</p>
		</div>

		<div class="mt-12 grid gap-5 sm:grid-cols-2 lg:grid-cols-4">
			{#each services as service (service.title)}
				<div
					class="group rounded-2xl bg-white p-6 ring-1 ring-brand-100 transition hover:-translate-y-1 hover:shadow-xl hover:ring-brand-300"
				>
					<div
						class="flex h-12 w-12 items-center justify-center rounded-xl bg-brand-100 text-brand-700 transition group-hover:bg-brand-300 group-hover:text-brand-900"
					>
						{#if service.icon === 'home'}
							<svg
								class="h-6 w-6"
								viewBox="0 0 24 24"
								fill="none"
								stroke="currentColor"
								stroke-width="2"
								stroke-linecap="round"
								stroke-linejoin="round"
								><path d="m3 9 9-7 9 7v11a2 2 0 0 1-2 2h-4v-7H9v7H5a2 2 0 0 1-2-2z" /></svg
							>
						{:else if service.icon === 'sparkles'}
							<svg
								class="h-6 w-6"
								viewBox="0 0 24 24"
								fill="none"
								stroke="currentColor"
								stroke-width="2"
								stroke-linecap="round"
								stroke-linejoin="round"
								><path
									d="M12 3v3M12 18v3M5.6 5.6l2.1 2.1M16.3 16.3l2.1 2.1M3 12h3M18 12h3M5.6 18.4l2.1-2.1M16.3 7.7l2.1-2.1"
								/><circle cx="12" cy="12" r="3" /></svg
							>
						{:else if service.icon === 'truck'}
							<svg
								class="h-6 w-6"
								viewBox="0 0 24 24"
								fill="none"
								stroke="currentColor"
								stroke-width="2"
								stroke-linecap="round"
								stroke-linejoin="round"
								><path d="M14 18V6H2v11h2" /><path d="M14 8h4l4 4v5h-2" /><circle
									cx="7"
									cy="18"
									r="2"
								/><circle cx="17" cy="18" r="2" /></svg
							>
						{:else if service.icon === 'key'}
							<svg
								class="h-6 w-6"
								viewBox="0 0 24 24"
								fill="none"
								stroke="currentColor"
								stroke-width="2"
								stroke-linecap="round"
								stroke-linejoin="round"
								><circle cx="7.5" cy="15.5" r="3.5" /><path
									d="m10 13 10-10M16 7l3 3M14 9l3 3"
								/></svg
							>
						{:else if service.icon === 'palette'}
							<svg
								class="h-6 w-6"
								viewBox="0 0 24 24"
								fill="none"
								stroke="currentColor"
								stroke-width="2"
								stroke-linecap="round"
								stroke-linejoin="round"
								><path
									d="M12 22a10 10 0 1 1 10-10c0 2-2 3-4 3h-1a2 2 0 0 0-1 4 2 2 0 0 1-2 3z"
								/><circle cx="6.5" cy="12" r="1" /><circle cx="9" cy="7.5" r="1" /><circle
									cx="14.5"
									cy="7"
									r="1"
								/><circle cx="18" cy="11" r="1" /></svg
							>
						{:else if service.icon === 'building'}
							<svg
								class="h-6 w-6"
								viewBox="0 0 24 24"
								fill="none"
								stroke="currentColor"
								stroke-width="2"
								stroke-linecap="round"
								stroke-linejoin="round"
								><rect x="4" y="3" width="16" height="18" rx="2" /><path
									d="M9 8h.01M15 8h.01M9 12h.01M15 12h.01M9 16h.01M15 16h.01"
								/></svg
							>
						{:else if service.icon === 'hammer'}
							<svg
								class="h-6 w-6"
								viewBox="0 0 24 24"
								fill="none"
								stroke="currentColor"
								stroke-width="2"
								stroke-linecap="round"
								stroke-linejoin="round"
								><path d="m15 12-8.5 8.5a2.12 2.12 0 0 1-3-3L12 9" /><path
									d="M17.64 15 22 10.64M20.91 11.7l-1.25-1.25c-.6-.6-.93-1.4-.93-2.25v-.86L16.01 4.6a5.55 5.55 0 0 0-3.94-1.6H9l.92.82A6.18 6.18 0 0 1 12 8.4v1.45l2.05 2.05c.85 0 1.65.33 2.25.93l1.25 1.25"
								/></svg
							>
						{:else if service.icon === 'clock'}
							<svg
								class="h-6 w-6"
								viewBox="0 0 24 24"
								fill="none"
								stroke="currentColor"
								stroke-width="2"
								stroke-linecap="round"
								stroke-linejoin="round"
								><circle cx="12" cy="12" r="10" /><path d="M12 6v6l4 2" /></svg
							>
						{/if}
					</div>
					<h3 class="mt-4 font-display text-xl text-brand-900">{service.title}</h3>
					<p class="mt-2 text-sm text-brand-900/70">{service.description}</p>
				</div>
			{/each}
		</div>
	</section>

	<!-- Pricing -->
	<section id="pricing" class="scroll-mt-24 bg-brand-50 py-20 md:py-28">
		<div class="mx-auto max-w-6xl px-5">
			<div class="grid gap-12 md:grid-cols-2 md:gap-16">
				<div>
					<p class="text-sm font-bold tracking-widest text-brand-500 uppercase">Pricing</p>
					<h2 class="mt-2 font-display text-4xl text-brand-900 md:text-5xl">
						Honest, custom pricing
					</h2>
					<p class="mt-4 text-lg text-brand-900/80">
						Every space is different. Pricing is customized based on:
					</p>
					<ul class="mt-4 space-y-2 text-brand-900/80">
						{#each ['Square footage', 'Property condition', 'Number of bedrooms & bathrooms', 'Frequency of service', 'Add-on requests'] as item (item)}
							<li class="flex items-start gap-3">
								<svg
									class="mt-1 h-4 w-4 flex-none text-brand-500"
									viewBox="0 0 24 24"
									fill="none"
									stroke="currentColor"
									stroke-width="3"
									stroke-linecap="round"
									stroke-linejoin="round"><polyline points="20 6 9 17 4 12" /></svg
								>
								<span>{item}</span>
							</li>
						{/each}
					</ul>
					<a
						href={emailHref}
						class="mt-8 inline-flex items-center gap-2 rounded-full bg-brand-700 px-6 py-3 font-bold text-white shadow-md transition hover:bg-brand-800"
					>
						Request a quote
						<svg
							class="h-4 w-4"
							viewBox="0 0 24 24"
							fill="none"
							stroke="currentColor"
							stroke-width="2.5"
							stroke-linecap="round"
							stroke-linejoin="round"
							><line x1="5" y1="12" x2="19" y2="12" /><polyline points="12 5 19 12 12 19" /></svg
						>
					</a>
				</div>

				<div class="rounded-3xl bg-white p-8 shadow-xl ring-1 ring-brand-100">
					<h3 class="font-display text-2xl text-brand-700">Starting Rates</h3>
					<ul class="mt-6 divide-y divide-brand-100">
						{#each pricing as row (row.label)}
							<li class="flex items-center justify-between gap-4 py-4">
								<span class="font-semibold text-brand-900">{row.label}</span>
								<span class="rounded-full bg-brand-100 px-3 py-1 font-display text-brand-700"
									>{row.price}</span
								>
							</li>
						{/each}
					</ul>
					<p class="mt-6 text-xs text-brand-900/60">
						Listed prices are starting points. Final pricing is provided after a quick consultation.
					</p>
				</div>
			</div>

			<div class="mt-16">
				<p class="text-sm font-bold tracking-widest text-brand-500 uppercase">Add-Ons</p>
				<h3 class="mt-2 font-display text-3xl text-brand-900 md:text-4xl">
					Customize your cleaning
				</h3>
				<div class="mt-8 grid gap-3 sm:grid-cols-2 lg:grid-cols-3">
					{#each addOns as addon (addon)}
						<div
							class="flex items-center gap-3 rounded-2xl bg-white px-5 py-4 ring-1 ring-brand-100"
						>
							<span
								class="flex h-8 w-8 flex-none items-center justify-center rounded-full bg-brand-300 text-brand-900"
							>
								<svg
									class="h-4 w-4"
									viewBox="0 0 24 24"
									fill="none"
									stroke="currentColor"
									stroke-width="3"
									stroke-linecap="round"
									stroke-linejoin="round"><polyline points="20 6 9 17 4 12" /></svg
								>
							</span>
							<span class="font-semibold text-brand-900">{addon}</span>
						</div>
					{/each}
				</div>
			</div>
		</div>
	</section>

	<!-- Pest Control -->
	<section id="pest" class="mx-auto max-w-6xl scroll-mt-24 px-5 py-20 md:py-28">
		<div class="grid items-center gap-12 md:grid-cols-5">
			<div class="md:col-span-3">
				<p class="text-sm font-bold tracking-widest text-brand-500 uppercase">Add-On</p>
				<h2 class="mt-2 font-display text-4xl text-brand-900 md:text-5xl">Pest Control Services</h2>
				<p class="mt-5 text-lg text-brand-900/80">
					We also offer pest control add-on services for homes, rental properties, Airbnb units, and
					businesses throughout San Antonio. Our preventative and treatment options help keep your
					space clean, comfortable, and pest-free.
				</p>
				<div class="mt-8 grid gap-3 sm:grid-cols-2">
					{#each pestServices as pest (pest)}
						<div
							class="flex items-center gap-3 rounded-2xl bg-white px-5 py-4 ring-1 ring-brand-100"
						>
							<span
								class="flex h-9 w-9 flex-none items-center justify-center rounded-full bg-brand-100 text-brand-700"
							>
								<svg
									class="h-5 w-5"
									viewBox="0 0 24 24"
									fill="none"
									stroke="currentColor"
									stroke-width="2"
									stroke-linecap="round"
									stroke-linejoin="round"
								>
									<path d="M12 2v4M8 6l-2-2M16 6l2-2" />
									<ellipse cx="12" cy="13" rx="5" ry="7" />
									<path d="M7 10H3M21 10h-4M7 16H3M21 16h-4M7 13H2M22 13h-5" />
								</svg>
							</span>
							<span class="font-semibold text-brand-900">{pest}</span>
						</div>
					{/each}
				</div>
				<p class="mt-6 text-sm text-brand-900/60">
					Available as standalone visits or bundled with a cleaning. Ask for current pricing.
				</p>
			</div>
			<div class="relative md:col-span-2" aria-hidden="true">
				<div
					class="absolute -inset-4 rounded-[2rem] bg-gradient-to-br from-brand-200 to-brand-400 opacity-40 blur-2xl"
				></div>
				<div
					class="relative flex flex-col gap-3 rounded-[2rem] bg-gradient-to-br from-brand-500 to-brand-700 p-8 text-white shadow-xl"
				>
					<svg
						class="h-12 w-12 text-brand-200"
						viewBox="0 0 24 24"
						fill="none"
						stroke="currentColor"
						stroke-width="1.8"
						stroke-linecap="round"
						stroke-linejoin="round"
					>
						<path d="M12 22a10 10 0 0 0 10-10V5l-10-3L2 5v7a10 10 0 0 0 10 10z" />
						<path d="m9 12 2 2 4-4" />
					</svg>
					<p class="font-display text-2xl leading-tight">
						Preventative care that keeps your space comfortable, year-round.
					</p>
					<p class="text-sm text-brand-100">
						Bundle pest control with your regular cleaning visits for a complete service.
					</p>
				</div>
			</div>
		</div>
	</section>

	<!-- Service Area -->
	<section id="area" class="mx-auto max-w-6xl scroll-mt-24 px-5 py-20 md:py-28">
		<div class="grid items-center gap-12 md:grid-cols-2">
			<div>
				<p class="text-sm font-bold tracking-widest text-brand-500 uppercase">Service Area</p>
				<h2 class="mt-2 font-display text-4xl text-brand-900 md:text-5xl">
					Greater San Antonio,<br />inside Loop 410
				</h2>
				<p class="mt-5 text-lg text-brand-900/80">
					We proudly serve homes and businesses throughout the city of San Antonio, TX — primarily
					inside the highway 410 loop. Just outside the loop? Reach out and we'll let you know if we
					can make it work.
				</p>
				<div class="mt-8 grid gap-4 sm:grid-cols-2">
					<div class="rounded-2xl bg-brand-50 p-5 ring-1 ring-brand-100">
						<p class="font-display text-lg text-brand-700">Residential</p>
						<p class="mt-1 text-sm text-brand-900/70">
							Houses, apartments, condos, and short-term rentals.
						</p>
					</div>
					<div class="rounded-2xl bg-brand-50 p-5 ring-1 ring-brand-100">
						<p class="font-display text-lg text-brand-700">Commercial</p>
						<p class="mt-1 text-sm text-brand-900/70">
							Offices, studios, and small businesses across the city.
						</p>
					</div>
				</div>
			</div>
			<div class="overflow-hidden rounded-3xl bg-white shadow-xl ring-1 ring-brand-100">
				<img
					src="{base}/map.png"
					alt="Map of the Raeleen Cleaning Co. service area in San Antonio, inside Loop 410."
					class="h-full w-full object-cover"
				/>
			</div>
		</div>
	</section>

	<!-- Why Choose -->
	<section id="why" class="scroll-mt-24 bg-brand-50 py-20 md:py-28">
		<div class="mx-auto max-w-6xl px-5">
			<div class="max-w-2xl">
				<p class="text-sm font-bold tracking-widest text-brand-500 uppercase">Why choose us</p>
				<h2 class="mt-2 font-display text-4xl text-brand-900 md:text-5xl">
					Why Raeleen Cleaning Co.
				</h2>
				<p class="mt-4 text-lg text-brand-900/80">
					Built around consistency, professionalism, and high-quality care — for the people and
					places that count on us most.
				</p>
			</div>

			<div class="mt-12 grid gap-5 sm:grid-cols-2 lg:grid-cols-3">
				{#each reasons as reason (reason.title)}
					<div class="rounded-2xl bg-white p-6 ring-1 ring-brand-100">
						<div
							class="flex h-10 w-10 items-center justify-center rounded-xl bg-brand-300 text-brand-900"
						>
							<svg
								class="h-5 w-5"
								viewBox="0 0 24 24"
								fill="none"
								stroke="currentColor"
								stroke-width="3"
								stroke-linecap="round"
								stroke-linejoin="round"
							>
								<polyline points="20 6 9 17 4 12" />
							</svg>
						</div>
						<h3 class="mt-4 font-display text-xl text-brand-900">{reason.title}</h3>
						<p class="mt-2 text-sm text-brand-900/70">{reason.description}</p>
					</div>
				{/each}
			</div>
		</div>
	</section>

	<!-- About -->
	<section id="about" class="scroll-mt-24 bg-gradient-to-b from-white to-brand-50 py-20 md:py-28">
		<div class="mx-auto grid max-w-6xl items-center gap-12 px-5 md:grid-cols-5">
			<div class="md:col-span-2">
				<div class="overflow-hidden rounded-3xl bg-white shadow-xl ring-1 ring-brand-100">
					<img
						src="{base}/raeleen.jpg"
						alt="Raeleen Torres"
						class="aspect-[4/5] w-full object-cover"
					/>
				</div>
			</div>
			<div class="md:col-span-3">
				<p class="text-sm font-bold tracking-widest text-brand-500 uppercase">Meet Raeleen</p>
				<h2 class="mt-2 font-display text-4xl text-brand-900 md:text-5xl">
					Welcome to Raeleen Cleaning Co.
				</h2>
				<p class="mt-5 text-lg text-brand-900/80">
					Raeleen Cleaning Co. is owned and operated by Raeleen Torres — a San Antonio local who
					built this business around three things: <span class="font-bold text-brand-700"
						>consistency, professionalism, and high-quality care.</span
					>
				</p>
				<p class="mt-4 text-lg text-brand-900/80">
					We specialize in creating fresh, welcoming spaces for homeowners, Airbnb hosts, studios,
					rental properties, and businesses. Whether you need a routine refresh, a deep clean, a
					move-in / move-out service, or an Airbnb turnover, our team is committed to making your
					space feel spotless, peaceful, and guest-ready.
				</p>
				<blockquote
					class="mt-8 border-l-4 border-brand-300 bg-white/70 py-3 pl-5 font-display text-xl text-brand-800"
				>
					We don't just clean spaces — we help create environments that feel refreshed, elevated,
					and ready for everyday life.
				</blockquote>
			</div>
		</div>
	</section>

	<!-- Contact / CTA -->
	<section id="contact" class="scroll-mt-24 bg-brand-700 py-20 text-white md:py-28">
		<div class="mx-auto max-w-4xl px-5 text-center">
			<p class="text-sm font-bold tracking-widest text-brand-200 uppercase">Get in touch</p>
			<h2 class="mt-2 font-display text-4xl md:text-6xl">Ready for a cleaner space?</h2>
			<p class="mx-auto mt-5 max-w-2xl text-lg text-brand-100">
				Tell us about your space and we'll put together a custom quote. Same-day cleans are
				sometimes available — just give us a call.
			</p>

			<div class="mt-10 grid gap-4 sm:grid-cols-2">
				<a
					href={phoneHref}
					class="group flex items-center justify-center gap-3 rounded-2xl bg-brand-300 px-6 py-5 text-brand-950 shadow-lg transition hover:bg-brand-200"
				>
					<svg
						class="h-6 w-6"
						viewBox="0 0 24 24"
						fill="none"
						stroke="currentColor"
						stroke-width="2"
						stroke-linecap="round"
						stroke-linejoin="round"
						><path
							d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07 19.5 19.5 0 0 1-6-6 19.79 19.79 0 0 1-3.07-8.67A2 2 0 0 1 4.11 2h3a2 2 0 0 1 2 1.72c.13.96.37 1.9.72 2.81a2 2 0 0 1-.45 2.11L8.09 9.91a16 16 0 0 0 6 6l1.27-1.27a2 2 0 0 1 2.11-.45c.91.35 1.85.59 2.81.72A2 2 0 0 1 22 16.92z"
						/></svg
					>
					<div class="text-left">
						<p class="text-xs font-bold tracking-widest uppercase opacity-70">Call or text</p>
						<p class="font-display text-2xl">{phone}</p>
					</div>
				</a>
				<a
					href={emailHref}
					class="group flex items-center justify-center gap-3 rounded-2xl bg-white px-6 py-5 text-brand-900 shadow-lg transition hover:bg-brand-50"
				>
					<svg
						class="h-6 w-6"
						viewBox="0 0 24 24"
						fill="none"
						stroke="currentColor"
						stroke-width="2"
						stroke-linecap="round"
						stroke-linejoin="round"
						><rect x="3" y="5" width="18" height="14" rx="2" /><path d="m3 7 9 6 9-6" /></svg
					>
					<div class="text-left">
						<p class="text-xs font-bold tracking-widest uppercase opacity-70">Email</p>
						<p class="font-display text-lg break-all">{email}</p>
					</div>
				</a>
			</div>
		</div>
	</section>

	<footer class="bg-brand-950 py-10 text-brand-200">
		<div
			class="mx-auto flex max-w-6xl flex-col items-center justify-between gap-4 px-5 text-sm md:flex-row"
		>
			<div class="flex items-baseline gap-2">
				<span class="font-display text-xl text-white">Raeleen</span>
				<span class="font-display text-lg text-brand-300">Cleaning Co.</span>
			</div>
			<p class="text-center text-brand-300/80">
				San Antonio, TX · Inside Loop 410 · &copy; {new Date().getFullYear()} Raeleen Cleaning Co.
			</p>
			<div class="flex items-center gap-4">
				<a class="hover:text-white" href={phoneHref}>{phone}</a>
				<span class="text-brand-700">·</span>
				<a class="hover:text-white" href={emailHref}>Email</a>
			</div>
		</div>
	</footer>
</div>
