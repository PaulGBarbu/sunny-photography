<script>
	import '../app.css';
	import Orig_GoldyChurch from '$lib/images/original/goldy-church.webp?enhanced';
	import Edit_GoldyChurch from '$lib/images/edit/goldy-church.webp?enhanced';

	import Orig_CloudySunset from '$lib/images/original/cloudy-sunset.jpeg?enhanced';
	import Edit_CloudySunset from '$lib/images/edit/cloudy-sunset.webp?enhanced';

	import Orig_Building1 from '$lib/images/original/building1.jpeg?enhanced';
	import Edit_Building1 from '$lib/images/edit/building1.webp?enhanced';

	import Orig_CapitalGreen from '$lib/images/original/capital_green.webp?enhanced';
	import Edit_CapitalGreen from '$lib/images/edit/capital_green.webp?enhanced';

	import Orig_ConcSlab from '$lib/images/original/concreate_slab.webp?enhanced';
	import Edit_ConcSlab from '$lib/images/edit/concreate_slab.webp?enhanced';

	import Switcher from '$lib/Switcher.svelte';
	import PhotoInfo from '$lib/PhotoInfo.svelte';

	let rowCSS = 'mx-auto justify-center px-4 flex flex-col sm:flex-row md:w-2/3 lg:w-1/2 md:px-0 ';
	let switcherCSS = 'flex aspect-2/3 justify-end w-full sm:w-1/2';
</script>

<div class="relative w-full bg-stone-900">
	<div class="dots h-[122px] pt-7 text-center text-3xl font-bold text-white">
		Sunnys & Pauli <br /> Photography
	</div>
	<div class="hatched-rev h-10"></div>

	<!-- Schraffur Link -->
	<div class="hatched absolute top-0 bottom-0 left-0 w-4 md:w-8"></div>
	<!-- Schraffur Rechts -->
	<div class="hatched absolute top-0 right-0 bottom-0 w-4 md:w-8"></div>

	<!-- Extra Lines -->
	<div>
		<div
			class="brdr-t2b pointer-events-none absolute top-40 bottom-0 z-10 hidden w-1/6 md:block lg:w-1/4"
		></div>
		<div
			class="brdr-t2b pointer-events-none absolute top-40 bottom-0 z-10 hidden w-1/2 sm:block"
		></div>
		<div
			class="brdr-t2b pointer-events-none absolute top-40 bottom-0 z-10 hidden w-5/6 md:block lg:w-3/4"
		></div>
	</div>

	<!-- Row 1 -->
	<div class={rowCSS}>
		<div class={switcherCSS}>
			<Switcher edit={Edit_GoldyChurch} original={Orig_GoldyChurch} />
		</div>
		<PhotoInfo
			photoBy={'Sunny'}
			editBy={'Pauli'}
			location={'Italy - Mailand'}
			date={'25.04.2025'}
		/>
	</div>

	<div class="hatched-rev h-6 w-full"></div>

	<!-- Row 2 -->
	<div class={rowCSS}>
		<PhotoInfo
			photoBy={'Sunny'}
			editBy={'Pauli'}
			location={'Germany - Rosenheim'}
			date={'29.04.2025'}
		/>
		<div class={switcherCSS}>
			<Switcher edit={Edit_CloudySunset} original={Orig_CloudySunset} />
		</div>
	</div>

	<div class="hatched-rev h-6 w-full"></div>

	<!-- Row 3 -->
	<div class={rowCSS}>
		<div class={switcherCSS}>
			<!-- <div class="text-white">Here goes an image</div> -->
			<Switcher edit={Edit_Building1} original={Orig_Building1} />
		</div>
		<PhotoInfo photoBy={'Sunny'} editBy={'Pauli'} />
	</div>

	<div class="hatched-rev h-6 w-full"></div>

	<!-- Row 4 -->
	<div class={rowCSS}>
		<PhotoInfo photoBy={'Sunny'} editBy={'Pauli'} location={'Singapur'} date={''} />
		<div class={switcherCSS}>
			<Switcher edit={Edit_CapitalGreen} original={Orig_CapitalGreen} />
		</div>
	</div>

	<div class="hatched-rev h-6 w-full"></div>

	<!-- Row 5 -->
	<div class={rowCSS}>
		<div class={switcherCSS}>
			<Switcher edit={Edit_ConcSlab} original={Orig_ConcSlab} />
		</div>
		<PhotoInfo photoBy={'Sunny'} editBy={'Pauli'} location={''} date={''} />
	</div>

	<div class="hatched-rev h-12 w-full"></div>
</div>
