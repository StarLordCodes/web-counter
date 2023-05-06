<script>
    import { count } from './stores.js';
    let countValue;
    count.subscribe(value => {countValue=value});
</script>

<div class="counter">
    <div class="counter-value"> {countValue} </div>
</div>

<style>
    .counter{
        grid-area: counter;
        align-self: center;
        justify-self: center;
    }
    .counter-value{
        font-size: 25rem;
        font-weight: 200;
    }
    @media (max-width:768px){
        .counter-value{
            font-size: 10rem;
        }
    }
    
</style>