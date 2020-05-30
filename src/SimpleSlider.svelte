<script>
    export let value = 5;
    export let min = 0;
    export let max = 10;
    export let step = 1;
</script>

<div class="slider-container">
    <input type="range" bind:value={value} min={min} max={max} step={step}>
    <span>{value}</span>
</div>

<style>
    .slider-container {
        display: flex;
        align-items: center;
    }
    input {
        margin:0 0.5em 0 0;
    }
</style>