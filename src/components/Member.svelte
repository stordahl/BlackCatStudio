<script>
    export let name;
    export let pronouns;
    export let desc;
    export let image;
</script>

<div class="member-row">
<div class="frame"><img src="{ image }" alt="portrait of { name }"></div>
    <div class="text-inner">
        <h2>{ name }</h2>
        <h4>{ pronouns }</h4>
        <p>{ desc }</p>
    </div> 
</div>

<style>
    .member-row{
        display:flex;
        flex-direction: column;
        align-items:center;
        margin-bottom:2.2rem;
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

    @media screen and (min-width:600px){
        .text-inner{
            max-width:60%;
        }
    }
    @media screen and (min-width:1000px){
        .member-row:nth-child(even){
            flex-direction:row-reverse;
        }
        .member-row:nth-child(odd){
            flex-direction: row;
        }
        .member-row:nth-last-child(odd) > .text-inner > *{
            text-align: right;
        }
        
    }
</style>