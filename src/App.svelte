<script>
	import Button from './Button.svelte';
	export const items = [
		{
			label: 'First item',
			position: 0,
		},
		{
			label: 'Second item',
			position: 1,
		},
		{
			label: 'Third item',
			position: 2,
		},
	];
</script>

{#each items as {label, position}}
	<Button>{label}</Button>
{/each}
