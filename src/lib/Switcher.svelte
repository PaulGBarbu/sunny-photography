<script>
	let { edit = $bindable(), original = $bindable() } = $props();

	let showEdit = $state(true);

	let imgClass = 'absolute inset-0 transition-opacity duration-[2s]  w-full h-full object-cover';
</script>

<button class="relative h-full w-full cursor-pointer" onclick={() => (showEdit = !showEdit)}>
	<!-- Edited (blurred) image shown by default -->
	<enhanced:img
		class={`${imgClass} ${showEdit ? 'opacity-100' : 'opacity-0'}`}
		src={edit}
		alt="Edited"
		loading="lazy"
	/>

	<!-- Original image, hidden until it loads -->
	<enhanced:img
		class={`${imgClass} ${showEdit ? 'opacity-0' : 'opacity-100'}`}
		src={original}
		alt="Original"
		loading="lazy"
		onload={() => (showEdit = true)}
	/>
</button>
