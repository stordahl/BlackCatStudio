<svelte:head>
	<title>Black Cat Studio</title>
</svelte:head>

<!-- javascript -->
<script>
	import { onMount } from 'svelte';
	import Arrow from '../components/Arrow.svelte';
	import Block from '../components/BlockHeading.svelte';
	import Form from '../components/MainForm.svelte';

	let headings = [
		{ heading: 'design', color: '#BB5215', },
		{ heading: 'development', color: '#DDA788', },
		{ heading: 'seo', color: '#A5C4E7', },
		{ heading: 'hosting', color: '#E6F2FF', },
		{ heading: 'maintenance', color: '#4E563E', },
		{ heading: 'support', color: '#999E90', },
	];

	let i = 0;
	let txt = 'not every website should be built the same.'; /* The text */
	let speed = 100;
	const typeWriter = () => {
		if(i < txt.length) {
			document.getElementById('typing').innerHTML += txt.charAt(i);
			i++;
		}
	}
	const typing = () =>{
		setInterval(typeWriter, speed);
	}
	const delay = () => {
		setTimeout(typing, speed*25)
	};
</script>

<svelte:window on:load={ delay }/>

<!-- markup -->
<Arrow />
<div class="content">
	<div class="full-right">
		<h1 id="headline">modern web <span class="striped-l-orange">design</span> and <span class="striped-d-blue">development</span> for small business</h1>
	</div>
	<div class="block-grid">
		<h1>offering...</h1>
		<div class="block-sub-grid">
			<Block {...headings[0]}/>
			<Block {...headings[1]}/>
			<Block {...headings[2]}/>
			<Block {...headings[3]}/>
			<Block {...headings[4]}/>
			<Block {...headings[5]}/>
		</div>		
	</div>
	<div id="main-text-cont">
			<hr>
				<div id="first-text">
					<h1 id="typing" style="margin-bottom:-1.5rem; margin-top:1rem; text-align:left; align-self:start;"> </h1>
					<p class="text" style="text-align: right; justify-self:end; max-width: 450px;">
						this is why we specialize in a variety of different technologies; 
						to be able to provide the most optimal solution for your business. 
					</p>
				</div>
			<hr>
			
			<img src="/yarn.png" alt="">
			
			<hr>
			<div class="click-through-cont">
				<p class="text">
					want a Wordpress site so you can easily manage content or 
					products? we’ve built a great deal of Wordpress sites 
					& would love to create a product that allows you to 
					control your own business online. 
				</p>
				<a href="/wp-landing"><button>free quote</button></a>
			</div>
			<hr>

			<img src="/mouse.png" alt="">

			<hr>
			<div class="click-through-cont two">
				<p class="text">
					need a small site to get the word out? maybe a 
					simple contact form to generate leads? we’ve created 
					a method of development for these use cases that is 
					quick to build and affordable to maintain & host. 
				</p>
				<a href="/static-landing"><button style="background-color:#BB5215;">free quote</button></a>
			</div>
			<hr>
	</div>
	<Form />
</div>

<!-- styles -->
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

.content{
	max-width: 100%;
}
#headline{
	text-align:right;
	max-width: 550px;
	font-size: 2.5rem;
}
#headline > span{
	display:inline;
	color:var(--black);
}
#headline > span:last-child{
	color:var(--black);
}
/* classes for underlines */
.striped-l-orange{
	background-image: linear-gradient(transparent 80%, var(--light-orange) 20%);
	background-size: 80px 50px;
	padding-bottom: 10px;
}
.striped-d-blue{
	background-image: linear-gradient(transparent 80%, var(--dark-blue) 20%);
	background-size: 80px 50px;
	padding-bottom: 10px;
}

.full-right{
	width:100%;
	display:flex;
	flex-direction:column; 
	align-items: center;
}
.block-grid{
	margin:auto;
}
.block-sub-grid{
	display:grid;
	grid-template-columns: auto;
	grid-template-rows: auto;
	justify-content: center;
}
#main-text-cont{
	display:flex;
	flex-direction:column;
	align-items: center;
	justify-content: center;
	
}
.text{
	padding: 1rem;
	max-width: 600px;
	font-size:1.25rem;
}
#first-text{
	display:grid;
	grid-template-columns:1fr;
	grid-template-rows: auto;
	width:100%;
	margin:1rem 0;
}
#main-text-cont > hr{
	width:75%;
	align-self:center;
}
#main-text-cont > img{
	max-width:300px;
}
.click-through-cont{
	display:flex;
	flex-direction: column;
	align-items: center;
	justify-content: center;
}
.click-through-cont button{
	width:12rem;
	height:2.5rem;
	background-color:var(--dark-green);
	color:white;
	box-shadow: 3px 3px 10px #1f1f1f36;
	border: none;
	font-size: 1.15rem;
	white-space: nowrap;
	cursor: pointer;
	font-style: italic;
}
.click-through-cont button:hover{
	scale:1.1;
}
.click-through-cont a{
	margin-bottom:2rem;
}

@media screen and (min-width:500px){
	#headline{
		margin: 5rem 0 9rem;
	}
}
@media screen and (min-width:660px){
	.block-grid{
		margin: 0 4rem;
	}
	.block-sub-grid{
		grid-template-columns: 1fr 1fr;
		margin-left: 6rem;
	}
}
@media screen and (min-width:800px){
	.full-right{
		align-items: flex-end
	}
	.click-through-cont{
		flex-direction: row;
	}
	.two{
		flex-direction:row-reverse;
	}
	.click-through-cont button{
		margin:.75rem;
	}
	#main-text-cont{
		margin:0 5rem;
	}
}
</style>