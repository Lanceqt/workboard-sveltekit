<script lang="ts">
    import { Drawer, drawerStore } from '@skeletonlabs/skeleton';
	import { InputChip } from '@skeletonlabs/skeleton';

	let list: string[] = ['Kasper', 'Camilla', 'karsten', 'Tobias'];
</script>

<Drawer position="right">
	{#if $drawerStore.id === 'assigments'}
	<pre class="pre">id: {$drawerStore.id}</pre>
		<button type="button" class="btn btn-l variant-filled">Opret opgave</button>

		<h2>Opgave 1</h2>
		<InputChip bind:value={list} name="chips" placeholder="Enter any value..." />

		<h2>Opgave 2</h2>
		<InputChip bind:value={list} name="chips" placeholder="Enter any value..." />

		<h2>Opgave 3</h2>
		<InputChip bind:value={list} name="chips" placeholder="Enter any value..." />

		<h2>Opgave 4</h2>
		<InputChip bind:value={list} name="chips" placeholder="Enter any value..." />
	{:else if $drawerStore.id === 'example-2'}
		<!-- (show 'example-2' contents) -->
		<pre class="pre">id: {$drawerStore.id}</pre>
	{:else}
	<pre class="pre">id: {$drawerStore.id}</pre>
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
