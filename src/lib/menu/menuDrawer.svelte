<script lang="ts">
    import { Drawer, drawerStore } from '@skeletonlabs/skeleton';
	import type { DrawerSettings } from '@skeletonlabs/skeleton';

	const drawerSettings: DrawerSettings = {
		id: 'example-22',
		width: 'w-[280px] md:w-[480px]',
		padding: 'p-4',
		rounded: 'rounded-xl',
	};
</script>

<Drawer position="right">
	{#if $drawerStore.id === 'example-1'}
		<!-- (show 'example-1' contents) -->
		1
	{:else if $drawerStore.id === 'example-2'}
		<!-- (show 'example-2' contents) -->
		2
	{:else}
		<form class="m-4" method="POST" action="/login">
			<label class="username m-4">
				<input class="input" title="Input (text)" type="text" placeholder="Brugernavn" />
			</label>
			<label class="password m-4">
				<input class="input" title="Input (text)" type="password" placeholder="Password" />
			</label>
			<button class="btn variant-filled mt-0 ml-4">Log in</button>
		</form>
	{/if}
</Drawer>
