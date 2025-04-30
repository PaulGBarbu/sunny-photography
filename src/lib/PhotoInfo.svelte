<script>
	let { photoBy = '', editBy = '', location = '', date = '' } = $props();
</script>

<div class="relative sm:w-1/2">
	<div class="brdr bottom-0 mx-auto flex h-20 w-full text-white sm:absolute">
		<div class="w-1/2">
			<div class="brdr h-2/3">
				<div class="ps-1 pt-1 text-xs font-bold">Photographed by</div>
				<div class="p-1">{photoBy}</div>
			</div>

			<div class="brdr h-1/3 p-1 text-xs">{location}</div>
		</div>
		<div class="w-1/2">
			<div class="brdr h-2/3">
				<div class="ps-1 pt-1 text-xs font-bold">Edited by</div>
				<div class="p-1">{editBy}</div>
			</div>
			<div class="brdr h-1/3 p-1 text-xs">{date}</div>
		</div>
	</div>
</div>
