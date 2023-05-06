<script>
    import {count} from './stores.js'
    const handleReset = () => {count.set(0)};
</script>

<div class="reset-btn">
    <button id="reset" on:click={handleReset}>Reset</button>
</div>

<style>
    .reset-btn{
        grid-area: reset-btn;
        align-self: center;
        justify-self: center;
    }
    #reset{
       font-size: 4rem;
       padding: 2rem 4rem;
       background-color: var(--button-color);
       color: white;
       border: 0.1rem solid white;
       font-weight: 200;
       opacity: 0.5;
    }
    #reset:hover{
        opacity: 1;
    } 
    #reset:active{
        background-color: rgb(83, 9, 9);
        transform: scale(0.99);
    }
    @media (max-width: 768px) {
       #reset{
            font-size: 2rem;
            width: 10rem;
            height: 8rem;
            padding: 1rem;
            align-self: center;
            justify-self: center;   
       }
    }
    
</style>