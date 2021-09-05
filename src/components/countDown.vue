<template>
      <div class="container p-1">
            <h4>Remaining</h4>
            <div class="counter">
                <div class="row">
                    <div class="col-1 circle" id="days"> </div>
                    <div class="col-1 circle" id="hours"> </div>
                    <div class="col-1 circle" id="mins"> </div>
                    <div class="col-1 circle" id="secs"> </div>
                </div>
                <div class="row">
                    <div class="col-1 words">DAYS</div>
                    <div class="col-1 words">HOURS</div>
                    <div class="col-1 words">MINS</div>
                    <div class="col-1 words">SECONDS</div>
                </div>
            </div>
        </div>
</template>

<script>
    var countDownDate = new Date("Jan 5, 2022 15:00:00").getTime();

    // Update the count down every 1 second
    var x = setInterval( function() {

    // Get today's date and time
    var now = new Date().getTime();

    // Find the distance between now and the count down date
    var diff = countDownDate - now;

    // Time calculations for days, hours, minutes and seconds
    var days = Math.floor(diff / (1000 * 60 * 60 * 24));
    var hours = Math.floor((diff % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
    var minutes = Math.floor((diff % (1000 * 60 * 60)) / (1000 * 60));
    var seconds = Math.floor((diff % (1000 * 60)) / 1000);

    // Display the result in the elements with id of "days","hours","minutes",seconds
    $("#days").text(days);
    $("#hours").text(hours);
    $("#mins").text(minutes);
    $("#secs").text(seconds);


    // If the count down is finished, write some text
    if (diff < 0)
    {
        clearInterval(x);
        $("#counter").text("EXPIRED");
    }
    }, 1000);
    export default {};
</script>

<style>
    h4
    {
        color: gray;
        font-weight: lighter;
    }

    .counter
    {
        font-family: Monospace;
        text-align: center;
    }

    .circle
    {   
        font-size: 40px;
        margin-right: 3px;
        height: 60px;
        background-color: black;
        border-radius: 100%;
        color: whitesmoke;
    }

    .words
    {
        margin-right: 3px;
    }
</style>