<script lang="ts">
	import { Ratings } from '@skeletonlabs/skeleton';
    import type { PageData } from './$types';
    let value = { current: 3.5, max: 5 };
    export let data: PageData;
</script>

<Ratings bind:value={value.current} max={value.max}>
	<svelte:fragment slot="empty">(icon)</svelte:fragment>
	<svelte:fragment slot="half">(icon)</svelte:fragment>
	<svelte:fragment slot="full">(icon)</svelte:fragment>
</Ratings>