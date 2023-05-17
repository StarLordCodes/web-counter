<script>
    import { rounds } from "./stores";
    $: bubbles = Array.from({ length: $rounds }, (_, i) => i + 1);
</script>

<div class="bubble-container">
    {#each bubbles as round}
    <div class="bubble">
        <p>{round}</p>
    </div>
    {/each}
</div>

<style>
    .bubble-container{
        align-self: center;
        justify-self: center;
        grid-area: bead;
        width: 22rem;
        display: flex;
        align-items: start;
        justify-content: center;
        flex-wrap: wrap;
    }
    .bubble{
        margin: 0.2rem;
        width: 2.5rem;
        height: 2.5rem;
        border: 0.1rem;
        border-radius: 100%;
        background-color: white;
        color:black;
        text-align: center;
        display: flex;
        align-items: center;
        justify-content: center;
    }
</style>