<script lang="ts">
	export let color: string;
	export let path: string;
	export let iconColor = 'white';
	export let size = 32;
	export let borderRadius: number | undefined = size * (6 / 32);
	export let round: boolean | undefined = undefined;
</script>

<svg
	viewBox="0 0 64 64"
	width={size}
	height={size}
	style:border-radius="{borderRadius}px"
	role="img"
	aria-label=""
>
	{#if round}
		<circle cx="32" cy="32" r="32" fill={color} />
	{:else}
		<rect width="64" height="64" fill={color} />
	{/if}

	<path d={path} fill={iconColor} />
</svg>
