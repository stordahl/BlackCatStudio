<script>
    export let name;
    export let pronouns;
    export let desc;
    export let image;
</script>

<div class="member-row">
    <div class="text-inner">
        <h2>{ name }</h2>
        <h4>{ pronouns }</h4>
        <p>{ desc }</p>
    </div> 
    <div class="frame"><img src="{ image }" alt="portrait of { name }"></div>
</div>

<style>
    .member-row{
        display:flex;
        align-items:center;
        margin-bottom:2.2rem;
    }
    .member-row:nth-last-child(even){
        flex-direction: row-reverse
    }
    .member-row:nth-last-child(even) > .text-inner > *{
        text-align: right;
    }
    .text-inner{
        max-width:60%;
    }
    .frame{
        width:300px;
        height:300px;
        border-radius: 50%;
        overflow: hidden;
        margin:1rem;
    }
    img{
        width:100%;
    }
</style>