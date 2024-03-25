<script lang="ts">
	import { Ratings } from '@skeletonlabs/skeleton';
	import Fa6SolidCircle from '~icons/fa6-solid/circle';
	import Fa6RegularCircle from '~icons/fa6-regular/circle';
    import type { PageData } from './$types';
	
    export let data: PageData;

    let value = { current: 2, max: 4 };
	

	//const hours = new Array(24).fill(null).map((_, i) => i + 1);
	const hours = new Array(24).fill(0);

	// function iconClick(event: CustomEvent<{index:number}>, hourState:number): void {
	// 	hourState = event.detail.index;
	// }
	
</script>

<h1>
	Today
</h1>

{#each hours as hourState}
	<Ratings bind:value={hourState} max={value.max} interactive on:icon={(e)=>(hourState = e.detail.index)}>
		<svelte:fragment slot="empty"><Fa6RegularCircle /></svelte:fragment>
		<svelte:fragment slot="full"><Fa6SolidCircle /></svelte:fragment>
	</Ratings>
{/each}

