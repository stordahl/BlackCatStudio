<script>
    export let heading;
    export let color;
</script>

<style>
    .square{
        width:30px;
        height:30px;
        margin-right:2rem;
    }
    .cont{
        margin:1.5rem 0;
        margin-right:.75rem;
        display:flex;
    }
    h3{
        font-size:1.75rem;
    }
</style>

<div class="cont">
    <div class="square" style="background-color:{ color }" ></div>
    <h3>{ heading }</h3>
</div>
