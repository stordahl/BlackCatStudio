<script>
	import { onMount } from 'svelte';
	export let segment;

	onMount( () => {
		// const page = document.getElementById('header') ;
		const logo = document.getElementById('logo-img');

		let vw = window.innerWidth;

		
			window.addEventListener("scroll", () => {
				if (vw >= 1000){
					const currentScroll = window.pageYOffset;
					if (currentScroll <= 10) {
					logo.style.scale = '1.25';
					} else if(currentScroll > 10){
						logo.style.scale = '1';
					}    
				}
			});
	});
	
</script>

<style>
	:root {
		--bg: #E0DCD8;
		--light-orange: #DDA788;
		--dark-orange:#BB5215;
		--light-blue:#E6F2FF;
		--dark-blue:#A5C4E7;
		--light-green: #999E90;
		--dark-green:#4E563E;
		--black:#1F1F1F;
	}
	header{
		display:flex;
		flex-direction: column;
		align-items: center;
	}
	nav {
		font-size:1.2rem;
		font-weight: 300;
	}
	ul {
		margin: auto;
		padding: 0;
		display:flex;
		justify-content: space-between;
		width: max-content;
		scale:0.6;
	}

	/* clearfix */
	ul::after {
		content: '';
		display: block;
		clear: both;
	}
	li {
		display: block;
		max-width:max-content;
		margin: 0 1rem;
	}
	[aria-current] {
		position: relative;
		display: inline-block;
	}
	li > a {
		text-decoration: none;
		padding: 1em 0.5em;
		display: block;
	}
	li > a:hover{
		scale:1.1;
	}
	.striped-d-orange{
		background-image: linear-gradient(transparent 80%, var(--dark-orange) 20%);
		background-size: 80px 45px;
		padding-bottom: 10px;
	}
	.striped-l-orange{
		background-image: linear-gradient(transparent 80%, var(--light-orange) 20%);
		background-size: 80px 45px;
		padding-bottom: 10px;
	}
	.striped-d-blue{
		background-image: linear-gradient(transparent 80%, var(--dark-blue) 20%);
		background-size: 80px 45px;
		padding-bottom: 10px;
	}
	.striped-l-blue{
		background-image: linear-gradient(transparent 80%, var(--light-blue) 20%);
		background-size: 80px 45px;
		padding-bottom: 10px;
	}
	.striped-l-green{
		background-image: linear-gradient(transparent 80%, var(--light-green) 20%);
		background-size: 80px 45px;
		padding-bottom: 10px;
	}
	#logo{
		display:flex;
		flex-direction: column;
		align-items:center;
		width:max-content;
		margin:auto;
	}
	#logo-main{
		width:100%;
	}
	#logo-sub{
		display: flex;
		justify-content: space-between;
		width:100%;
	}
	 h1{
		font-size:2rem;
		line-height:1;
		text-align:right;
		margin:0;
		padding:0;
	}
	h6{
		display:inline-block;
		font-size:1rem;
	}
	img{
		max-width:150px;
		margin:auto;
		transition: all .7s ease;
	}
	
	@media screen and (min-width:400px){
		ul{
			scale:0.8;
		}
	}
	@media screen and (min-width:500px){
		ul{
			scale:1;
		}
		#logo{
			flex-direction: row;
			align-items: center;
			justify-content: space-between;
			width: 90%;
			margin: 0 2rem;
		}
		img{
			width:120px;
			margin:0;
		}
	}
	@media screen and (min-width:600px){
		h1{font-size:2.5rem;}
	}
	@media screen and (min-width:750px){
		#logo{
			 margin: 0 3rem; 
		}
	}
	@media screen and (min-width:1000px){
		nav{
		padding: 0 1em;
		position: fixed;
		top:1rem;
		left:1rem;
		}
		ul{
			flex-direction:column;
		}
		header{
			align-items: flex-end;
		}
		#logo{
			width: 80%;
			margin: 2rem 4rem 2rem 15rem;
		}
		img{
			scale:1.25;
		}
		h1{font-size:3.5rem;}
		h6{font-size:1.5rem;}
	}
	@media screen and (min-width:1200px){
		#logo-img{
			position: fixed;
			top:2rem;
			right:3rem;
		}
	}
</style>

<header id="header">
	<nav>
		<ul>
			<li><a aria-current="{segment === undefined ? 'page' : undefined}" class="striped-d-orange" href=".">home</a></li>
			<li><a aria-current="{segment === 'services' ? 'page' : undefined}" class="striped-l-orange" href="services">services</a></li>
			<li><a aria-current="{segment === 'team' ? 'page' : undefined}" class="striped-d-blue" href="team">our team</a></li>
			<li><a aria-current="{segment === 'values' ? 'page' : undefined}" class="striped-l-blue" href="values">our values</a></li>
			<li><a rel=prefetch aria-current="{segment === 'blog' ? 'page' : undefined}" class="striped-l-green" href="blog">blog</a></li>
		</ul>
	</nav>
	<div id="logo">
		<div id="logo-text">
			<div id="logo-main">
				<h1>black cat studio</h1>
			</div>
			<div id="logo-sub">
				<h6>st. paul, mn</h6>
				<h6>est. 2020</h6>
			</div>
		</div>
		<a href="/"><img id="logo-img" src="/logo.png" alt=""></a>
	</div>
</header>
