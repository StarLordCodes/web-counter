<script>
    import {count} from './stores.js'
     const handleCount = ()=>{
        count.update(n => n += 1);
    }
</script>

<div class="add-btn">
    <button id="count-up" on:click={handleCount}>Count</button>
</div>

<style>
    .add-btn{
        grid-area: add-btn;
        align-self: center;
        justify-self: center;
    }
    #count-up{
       font-size: 4rem;
       padding: 2rem 4rem;
       background-color: var(--button-color);
       color:white;
       border: 0.1rem solid white;
       font-weight: 200;
       opacity: 0.5;
    }
    #count-up:hover{
        opacity: 1;
    }
    #count-up:active{
        background-color: rgb(5, 70, 5);
        transform: scale(0.99);
    }
    @media (max-width: 768px) {
        #count-up {
            font-size: 2rem;
            width: 10rem;
            height: 8rem;
            padding: 1rem;
            align-self: center;
            justify-self: center;
        }
    }
    
</style>