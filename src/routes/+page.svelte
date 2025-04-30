<script>
	import '../app.css';
	import Orig_GoldyChurch from '$lib/images/original/goldy-church.webp?enhanced';
	import Edit_GoldyChurch from '$lib/images/edit/goldy-church.webp?enhanced';

	import Orig_CloudySunset from '$lib/images/original/cloudy-sunset.jpeg?enhanced';
	import Edit_CloudySunset from '$lib/images/edit/cloudy-sunset.webp?enhanced';

	import Orig_Building1 from '$lib/images/original/building1.jpeg?enhanced';
	import Edit_Building1 from '$lib/images/edit/building1.webp?enhanced';

	import Switcher from '$lib/Switcher.svelte';
	import PhotoInfo from '$lib/PhotoInfo.svelte';
</script>

<div class="relative w-full bg-stone-900">
	<div
		class="graph-paperx dots h-[100px] bg-red-500 pt-7 text-center text-3xl font-bold text-white"
	>
		Sunnys & Pauli Photography
	</div>
	<div class="hatched-rev h-10"></div>

	<!-- Schraffur Link -->
	<div class="hatched absolute top-0 bottom-0 left-0 w-4 md:w-8"></div>
	<!-- Schraffur Rechts -->
	<div class="hatched absolute top-0 right-0 bottom-0 w-4 md:w-8"></div>

	<!-- Extra Lines -->
	<div class="">
		<div
			class="brdr-t2b pointer-events-none absolute top-35 bottom-0 z-10 hidden w-1/4 md:block"
		></div>
		<div
			class="brdr-t2b pointer-events-none absolute top-35 bottom-0 z-10 hidden w-1/2 sm:block"
		></div>
		<div
			class="brdr-t2b pointer-events-none absolute top-35 bottom-0 z-10 hidden w-3/4 md:block"
		></div>
	</div>

	<!-- Row 1 -->
	<div class="mx-auto justify-center px-4 sm:flex md:w-1/2 md:px-0">
		<div class="flex aspect-2/3 justify-end overflow-clip sm:w-1/2">
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
	<div class="mx-auto flex justify-center px-4 md:w-1/2 md:px-0">
		<PhotoInfo
			photoBy={'Sunny'}
			editBy={'Pauli'}
			location={'Germany - Rosenheim'}
			date={'29.04.2025'}
		/>
		<div class="flex aspect-2/3 w-1/2 justify-end overflow-clip">
			<Switcher edit={Edit_CloudySunset} original={Orig_CloudySunset} />
		</div>
	</div>

	<div class="hatched-rev h-6 w-full"></div>

	<!-- Row 3 -->

	<div class="mx-auto flex justify-center px-4 md:w-1/2 md:px-0">
		<div class="flex aspect-2/3 w-1/2 justify-end overflow-clip">
			<!-- <div class="text-white">Here goes an image</div> -->
			<Switcher edit={Edit_Building1} original={Orig_Building1} />
		</div>
		<PhotoInfo photoBy={'Sunny'} editBy={'Pauli'} />
	</div>

	<div class="hatched-rev h-12 w-full"></div>
</div>
