<script></script>

<style>
    #form-cont{
        width:100%;
        max-width:90vw;
        display:grid;
        justify-content: center;
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
    input, textarea, button{
        border:none;
        box-shadow:3px 3px 5px #1f1f1f36;
        background-color:white;
        padding:.25rem .75rem;
        font-size:1.25rem;
        line-height:1;
        color:#4E563E;
    }
    textarea{
        resize: none;
    }
    h5{
        font-size: 1.5rem;
    }
    h5 > span{
        font-size:1.15rem;
    }
    @media screen and (min-width:700px){
        form{
            grid-template-columns: 1fr 1fr;
            grid-template-rows: 1fr 1.25fr 1.25fr;
            grid-template-areas: 
                "name phone"
                "email message"
                "submit message";
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
        textarea[name="message"]{
            grid-area:message;
        }
        button{
            grid-area: submit;
            height:2rem;
            width:60%;
            align-self: flex-end;
        }
    }
</style>

<div id="form-cont">
    <h5>say howdy! - <span>we'd love to chat about how we can help you accomplish your goals online</span></h5>
    <form action="">
        <input type="text" name="name" placeholder="name">
        <input type="tel" name="phone" placeholder="phone">
        <input type="email" name="email" placeholder="email">
        <textarea name="message" id="message-text-area" cols="30" rows="3" placeholder="message"></textarea>
        <button type="submit">submit</button>
    </form>
</div>