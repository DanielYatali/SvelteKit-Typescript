<script lang="ts">
	let x: number = 0;

	const clicked = () => {
		x += 1;
	};

	let textArray: string[] = ['Hello', 'World', 'Svelte', 'Kit'];

	const reArrange = () => {
		textArray = textArray.slice(1).concat(textArray[0]);
	};
</script>

<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>
<button on:click|preventDefault={clicked}>clicked {x} times</button>
<p>{textArray}</p>
<button on:click|preventDefault={reArrange}>re-arrange</button>
