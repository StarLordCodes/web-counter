<script>
	import Add from "../components/Add.svelte";
	import Counter from "../components/Counter.svelte";
	import Date from "../components/Date.svelte";
	import Reset from "../components/Reset.svelte";

</script>

<div class="main-container">
    <Date/>
    <Counter/>
    <Add/>
    <Reset/>
</div>

<style>
    
    @import url('https://fonts.googleapis.com/css2?family=Noto+Sans:wght@200;300;400&display=swap');

    :global(body,html) {
        margin:0;
        padding:0;
    }
    :root{
        --primary-color: rgb(17, 16, 16);
        --button-color: rgb(20,16,16)
    }
    .main-container{
        font-family: 'Noto Sans', sans-serif;
        background-color: var(--primary-color);
        height:100vh;
        color: white;
        display: grid;
        grid-template-columns: 2fr 1fr; 
        grid-template-rows: 1fr 1fr 1fr; 
        gap: 0px 0px; 
        grid-template-areas: 
            "counter today"
            "counter add-btn"
            "counter reset-btn"; 
        align-items: center;
        justify-content: center;
    }

    @media (max-width: 768px) {
        .main-container{
        font-family: 'Noto Sans', sans-serif;
        background-color: var(--primary-color);
        height:100vh;
        width: 100vw;
        color: white;
        display: grid;
        grid-template-columns: 1fr 1fr; 
        grid-template-rows: 1fr 3fr 2fr ; 
        gap: 0px 0px; 
        grid-template-areas: 
            "today today"
            "counter counter"
            "add-btn reset-btn"; 
        align-items: center;
        justify-content: center;
    }
        
}
</style>