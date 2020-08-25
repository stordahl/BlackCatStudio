<svelte:head>
	<title>Black Cat Studio: Our Services</title>
</svelte:head>

<!-- javascript -->
<script>
	import Arrow from '../components/Arrow.svelte';
	import Block from '../components/BlockHeading.svelte';
	import Form from '../components/MainForm.svelte';

	let services = [
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
	<h1>our services are...</h1>
	<div id="services-cont">
		<div class="sub-cont">
			<Block {...services[0]}/>
			<p>full web mockups | interactive prototypes | graphic design & branding | illustration</p>
		</div>
		<div class="sub-cont">
			<Block {...services[1]}/>
			<p>Wordpress | server-less modern JAMstack sites | Node.js app development</p>
		</div>
		<div class="sub-cont">
			<Block {...services[2]}/>
			<p>seo services | Google Business account management | seo driven development</p>
		</div>
		<div class="sub-cont">
			<Block {...services[3]}/>
			<p>Siteground Wordpress Hosting | Netlify server-less deployment | Node.js deployment</p>
		</div>
		<div class="sub-cont">
			<Block {...services[4]}/>
			<p>error logging & monitoring | web master | content management & editing</p>
		</div>
		<div class="sub-cont">
			<Block {...services[5]}/>
			<p>24/7 chat support | phone & email support 9-5 CST M-F</p>
		</div>
	</div>

	<hr>

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
		display:flex;
		flex-direction:column;
		align-items:center;
	}
	#services-cont{
		padding-left: 2rem;
	}
	h1{
		width:100%;
	}
	hr{
		margin:4rem 0;
		width:400px;
		max-width:80%;
		align-self: center;
	}
	p{
		margin-top:0;
		margin-bottom:2.5rem;
		font-size:1.25rem;
		max-width:80%;
	}

	@media screen and (min-width:800px){
		p{
			font-size: 1.2rem;
			max-width:100%;
		}
	}
</style>