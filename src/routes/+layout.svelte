<script lang='ts'>
	// The ordering of these imports is critical to your app working properly
	import '@skeletonlabs/skeleton/themes/theme-skeleton.css';
	// If you have source.organizeImports set to true in VSCode, then it will auto change this ordering
	import '@skeletonlabs/skeleton/styles/skeleton.css';
	// Most of your app wide CSS should be put in this file
	import '../app.postcss'
	import { AppShell } from '@skeletonlabs/skeleton';
	import { AppBar } from '@skeletonlabs/skeleton';
	import Menu from '$lib/menu/menuDrawer.svelte';
	import OpenMenu from '$lib/menu/openMenu.svelte';
 </script>
<Menu />
<AppShell>
	<svelte:fragment slot="header">
		<AppBar>
			<svelte:fragment slot="lead">
				<h1 class="h1"><span class="gradient-heading">Rikovas totalt seje arbejdstavle</span></h1>
			</svelte:fragment>
			<svelte:fragment slot="trail">
				<OpenMenu />
			</svelte:fragment>
		</AppBar>
	</svelte:fragment>
	<slot />
</AppShell>
