<svelte:head>
	<title>Black Cat Studio</title>
</svelte:head>

<!-- javascript -->
<script>
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
</script>

<!-- markup -->
<Arrow />
<div class="content">
	<div class="full-right">
		<h1 id="headline">modern web <span>design</span> and <span>development</span> for small business</h1>
		<hr id="headline-hr">
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
				<p class="text">
					we understand that not every website should be built the same. 
					this is why we specialize in a variety of different technologies; 
					to be able to provide the most optimal solution for your business. 
				</p>
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
				<button>free quote</button>
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
				<button style="background-color:#BB5215;">free quote</button>
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
	width:100%;
}
#headline{
	text-align:right;
	max-width: 550px;
	/* margin-right:4rem; */
	font-size: 2.5rem;
}
#headline > span{
	display:inline;
	color:var(--dark-green);
	text-shadow: 3px 3px 6px #1f1f1f54;
}
.full-right{
	width:100%;
	display:flex;
	flex-direction:column; 
	align-items: center;
}
#headline-hr{
	width:600px;
	max-width:80vw;
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
	margin:0 5rem;
}
.text{
	padding: 1rem;
	max-width: 600px;
	font-size:1.25rem;
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
.click-through-cont > button{
	width:20rem;
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
.click-through-cont > button:hover{
	scale:1.1;
}

@media screen and (min-width:500px){
	#headline{
		margin: 7rem 0;
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
	.click-through-cont > button{
		margin:.75rem;
	}
}
</style>