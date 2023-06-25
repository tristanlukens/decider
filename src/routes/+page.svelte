<script lang="ts">
	let val: string;
	const handleClick = () => {
		const rand = Math.random();
		if (rand >= 0.5) {
			val = 'Yes';
		} else {
			val = 'No';
		}
	};
</script>

<main class="h-screen flex justify-center items-center flex-col space-y-4">
	<h1 class="font-bold text-3xl">Decider</h1>
	<button
		on:click={handleClick}
		class="uppercase px-2 py-1 bg-green shadow rounded tracking-wider bg-sky-500 active:bg-sky-600 active:translate-y-0.5 hover:-translate-y-0.5 transition text-white font-bold"
		>decide</button
	>
	<hr class="w-48" />
	{#if val}
		<p class="font-bold">{val}</p>
	{:else}
		<p class="text-neutral-400 italic">Click the button!</p>
	{/if}
</main>
