<script>
	import toast, { Toaster } from 'svelte-french-toast';

	function handleClick(pos) {
		toast(`Testing the toast in ${pos}`,{
			position: pos
		});
	}
</script>

<main>
<Toaster />

<button on:click={() => handleClick('top-right')} >top-right</button>
<button on:click={() => handleClick('bottom-center')} >bottom-center</button>

</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>