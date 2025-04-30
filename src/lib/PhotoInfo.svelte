<script>
	let { photoBy = '', editBy = '', location = '', date = '' } = $props();
</script>

<div class="relative order-2 h-26 text-white sm:h-auto sm:w-1/2">
	<!-- Info Box -->
	<div class="absolute bottom-0 h-26 w-full">
		<!-- Row 1 -->
		<div class="flex h-2/4">
			<div class="brdr w-2/3">
				<div class="ps-1 pt-1 text-xs">Photographed by</div>
				<div class="p-1">{photoBy}</div>
			</div>
			<div class="brdr w-1/3">
				<div class="ps-1 pt-1 text-xs">Edited by</div>
				<div class="p-1">{editBy}</div>
			</div>
		</div>
		<!-- Row 2 -->
		<div class="flex h-1/4">
			<div class="brdr w-2/3 p-1 text-xs"></div>
			<div class="brdr w-1/3 p-1 text-xs">{date}</div>
		</div>
		<!-- Row 3 -->
		<div class="flex h-1/4">
			<div class="brdr w-full p-1 text-xs">{location}</div>
		</div>
	</div>
</div>
