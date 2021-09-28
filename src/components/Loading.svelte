<script>
    import { fly } from "svelte/transition";

    let loading = true;

    setTimeout(() => {
        loading = false;
    }, 2500);
</script>

{#if loading}
    <div class="loading-overlay" transition:fly={{ y: -1000, duration: 700 }}>
        <h1>Hang Tight...</h1>
        <!-- <button
            on:click={() => {
                loading = false;
            }}
        >
            Stop Loading
        </button> -->
    </div>
{/if}

<style>
    .loading-overlay {
        position: fixed;
        left: 0;
        right: 0;
        top: 0;
        bottom: 0;
        background-color: slateblue;
        z-index: 1;
        display: flex;
        align-items: center;
        justify-content: center;
    }
</style>
