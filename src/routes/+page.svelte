<script>
	import Counter from "../components/Counter.svelte";
	import Date from "../components/Date.svelte";

</script>

<div class="main-container">
    <Date/>
    <Counter/>
</div>

<style>
    
    @import url('https://fonts.googleapis.com/css2?family=Noto+Sans:wght@200;300;400&display=swap');

    :global(body,html) {
        margin:0;
        padding:0;
    }
    .main-container{
        font-family: 'Noto Sans', sans-serif;
        background-color: rgb(17, 16, 16);
        height:100vh;
        color: white;
        display: grid; 
        grid-auto-columns: 1fr; 
        grid-template-columns: 1fr 2fr; 
        grid-template-rows: 1fr 1fr 1fr; 
        gap: 0px 0px; 
        grid-template-areas: 
            "day counter"
            "month counter"
            "year counter"; 
}
</style>