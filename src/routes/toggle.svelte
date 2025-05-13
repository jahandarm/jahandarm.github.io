<script lang="ts">
    import { fly } from 'svelte/transition'
    import { Moon, Sun } from 'lucide-svelte'
    import { theme } from '$lib/theme.svelte'
</script>

<button class="cursor-pointer" on:click={theme.toggle} aria-label="Toggle theme">
    {#if theme.current === 'dark'}
        <div in:fly={{ y: 10 }}>
            <Sun />
        </div>
    {:else}
        <div in:fly={{ y: -10 }}>
            <Moon />
        </div>
    {/if}
</button>
