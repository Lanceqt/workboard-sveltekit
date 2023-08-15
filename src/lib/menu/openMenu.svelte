<script lang="ts">
    import { drawerStore } from '@skeletonlabs/skeleton';
    import type { DrawerSettings } from '@skeletonlabs/skeleton';
    import LeftArrow from '$lib/icons/leftArrow.svelte';

    const drawerSettings: DrawerSettings = {
            id: 'assigments',
            width: 'w-[280px] md:w-[480px]',
            padding: 'p-4',
            rounded: 'rounded-xl',
        };
    function drawerOpen(): void {
            drawerStore.open(drawerSettings);
        }
</script>

<div class="cursor-pointer" on:click={drawerOpen} on:keypress={drawerOpen}><LeftArrow /></div>