<script lang="ts">
    import { Drawer, drawerStore } from '@skeletonlabs/skeleton';
    import type { DrawerSettings } from '@skeletonlabs/skeleton';
    import LeftArrow from '$lib/icons/leftArrow.svelte';

    const drawerSettings: DrawerSettings = {
            id: 'example-22',
            width: 'w-[280px] md:w-[480px]',
            padding: 'p-4',
            rounded: 'rounded-xl',
        };
    function drawerOpen(): void {
            drawerStore.open(drawerSettings);
        }
</script>

<div class="cursor-pointer" on:click={drawerOpen} on:keypress={drawerOpen}><LeftArrow /></div>