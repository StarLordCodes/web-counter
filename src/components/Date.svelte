<script>
    const today = new Date();
    const day = String(today.getDate()).padStart(2, '0');
    const month = String(today.getMonth() + 1).padStart(2, '0'); // January is 0!
    const year = String(today.getFullYear()).slice(-2);

    const formattedDate = `${day}-${month}-${year}`;
</script>

<div class="day">
    {day}
</div>
<div class="month">
    {month}
</div>
<div class="year">
    {year}
</div>

<style>
    .day,.month,.year{
        font-size: 8rem;
        font-weight: 200;
        opacity: 50%;
        padding-left: 2rem;
    }
    .day{
        grid-area: day;
        align-self: end;
    }
    .month{
        grid-area: month;
        align-self: start;
    }
    .year{
        grid-area: year;
        align-self: start;
    }
</style>