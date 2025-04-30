<script>
	import '../app.css';
	import Orig_GoldyChurch from '$lib/images/original/goldy-church.webp?enhanced';
	import Edit_GoldyChurch from '$lib/images/edit/goldy-church.webp?enhanced';
	import Switcher from '$lib/Switcher.svelte';
</script>

<div class="w-96">
	<Switcher edit={Edit_GoldyChurch} original={Orig_GoldyChurch} />
</div>
