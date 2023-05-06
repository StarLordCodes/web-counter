<script>
    const today = new Date();
    const day = String(today.getDate()).padStart(2, '0');
    const month = String(today.getMonth() + 1).padStart(2, '0'); // January is 0!
    const year = String(today.getFullYear()).slice(-2);

    const formattedDate = `${day}-${month}-${year}`;
</script>
<div class="today">
{formattedDate}
</div>
<style>
    .today {
        font-size: 4rem;
        font-weight: 200;
        opacity: 50%;
        grid-area: today;
        align-self: center;
        justify-self: center;
    }
    .today:hover{
        opacity: 1;
    }
    @media (max-width:768px){
        .today{
            font-size: 2rem;
            align-self: start;
        }
    }
</style>