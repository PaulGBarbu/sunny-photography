<script>
	let { edit = $bindable(), original = $bindable() } = $props();
	let showEdit = $state(true);

	let imgClass = 'w-full rounded';
</script>

<button onclick={() => (showEdit = !showEdit)}>
	{#if showEdit}
		<div>
			<!-- Doesnt Work on gh-pages -->
			<enhanced:img class={imgClass} src={edit} alt="" srcset="" />
		</div>
	{:else}
		<div>
			<!-- Doesnt Work on gh-pages -->
			<enhanced:img class={imgClass} src={original} alt="" srcset="" />
		</div>
	{/if}
</button>
