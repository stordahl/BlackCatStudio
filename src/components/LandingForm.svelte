<script>
    export let text;
    export let name;
</script>

<div id="form-cont" netlify>
    <h1>interested in a { text }?</h1>
    <h5>drop us a line below to get the process started!</h5>
    <form name="{ name }">
        <input type="text" name="name" placeholder="name">
        <input type="tel" name="phone" placeholder="phone">
        <input type="email" name="email" placeholder="email">
        <button type="submit">submit</button>
    </form>
</div>

<style>
    #form-cont{
        width:100%;
        display:grid;
        justify-content: center;
        align-items: center;
        margin-top:2rem;
        margin-bottom:4rem;
    }
    form{
        max-width: 500px;
        margin: 2rem auto;
        display:grid;
        grid-template-columns: 1;
        grid-template-rows: auto;
        gap: 1rem;
        justify-content: center;
    }
    input, button{
        border:none;
        box-shadow:3px 3px 5px #1f1f1f36;
        background-color:white;
        padding:.25rem .75rem;
        font-size:1.25rem;
        line-height:1;
        color:#4E563E;
    }
    h1, h5{
        text-align:center;
    }
    h5{
        font-size: 1.25rem;
    }
    @media screen and (min-width:700px){
        form{
            grid-template-columns: 1fr 1fr;
            grid-template-rows: 1fr 1fr;
            grid-template-areas: 
                "name phone"
                "email submit";
            gap: 1.25rem;
        }
        input{
            max-height:2rem;
        }
        input[name="name"]{
            grid-area:name;
        }
        input[name="phone"]{
            grid-area:phone;
        }
        input[name="email"]{
            grid-area:email;
        }
        button{
            grid-area: submit;
            justify-self: flex-end;
            height:2rem;
            width:60%;
            align-self: flex-end;
        }
    }
</style>