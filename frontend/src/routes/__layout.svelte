<script context="module">
	export const load = async ({ url, params }) => ({
		props: {
			key: url
		}
	});
</script>

<script>
	import { fly } from 'svelte/transition';
	import { quintOut } from 'svelte/easing';

	export let key;
</script>

<div>
	<a href="/" style="position: fixed;top:0;">main</a>
	{#key key}
		<div
			out:fly={{ y: 10, duration: 500, easing: quintOut }}
			in:fly={{ y: 20, duration: 500, easing: quintOut }}
			style="position: absolute;top:60px;"
		>
			<slot />
		</div>
	{/key}
</div>
