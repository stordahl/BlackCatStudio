<style>
    ul {
        width:100vw;
        display:flex;
        flex-direction:column;
        justify-content: center;
		margin: 0;
        padding: 0;
        /* position: absolute;
        bottom: 1rem; */
	}
    li{
        display:inline;
        margin:0 1rem;
    }
    #pipe{
        display:none;
    }
	/* clearfix */
	ul::after {
		content: '';
		display: block;
		clear: both;
    }
    a, li{
        font-size:.85rem;
    }
    a:hover{
		text-decoration:underline;
	}
    #copyright{
        display: inline;
    }
    @media screen and (min-width:500px){
        footer{
            margin: 1.25rem 0;
        }
        ul{
            flex-direction:row;
        }
         #pipe{
            display:block;
        }
    }
</style>

<footer>
    <ul>
        <li>copyright 2020 <a id="copyright" href="https://blkcatstudio.com">blkcatstudio(.com)</a></li>
        <li id="pipe"> | </li>
        <li><a href="https://twitter.com/BlkCatStudio">twitter</a></li>
        <li><a href="https://instagram.com/blkcat.studio">instagram</a></li>
    </ul>
</footer>