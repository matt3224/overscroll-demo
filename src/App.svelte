<script>
	let scrollY = 0
	let innerHeight = 0
	let outerHeight = 0
	
	$: scrollHeight = outerHeight - innerHeight - 50
</script>
<svelte:window bind:scrollY bind:innerHeight bind:outerHeight />
<div>
	scroll: {scrollY}<br>
	height: {scrollHeight}<br>
	overscroll: {scrollY > scrollHeight || scrollY < 0}
</div>

<style>
	:global(body) {
		height: 1000px
	}
	div {
		position: sticky;
		top: 0;
	}
</style>