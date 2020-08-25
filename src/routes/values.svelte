<svelte:head>
	<title>Black Cat Studio: Our Values</title>
</svelte:head>

<!-- javascript -->
<script>
	import Arrow from '../components/Arrow.svelte';
	import Block from '../components/BlockHeading.svelte';
	import Form from '../components/MainForm.svelte';

	let values = [
		{ heading: 'security', color: '#BB5215', },
		{ heading: 'communication & transparency', color: '#A5C4E7', },
		{ heading: 'inclusion', color: '#4E563E', },
		{ heading: 'equity', color: '#999E90', },
	];
</script>

<!-- markup -->
<Arrow />
<div class="content">
	<h1>our values are...</h1>
	<div id="values-cont">
		<div class="sub-cont">
			<Block {...values[0]}/>
			<p>
				we know that online security is safety in the digital age, so your security is our top priority.
				we are always working to keep our security practices up-to-date with industry standards. the security 
				of your website is also the security of you customers personal information; we take personal care to 
				ensure that your customers data is safe.
			</p>
		</div>
		<div class="sub-cont">
			<Block {...values[1]}/>
			<p>
				at Black Cat Studio, we prioritize building client relationships that are based on clear
				communication & complete transparency. we will work diligently to make sure you have all
				the information you need, every step of the way, all explained using non-technical language.
			</p>
		</div>
		<div class="sub-cont">
			<Block {...values[2]}/>
			<p>
				when working with individuals outside of BCS, we always prioritize providing opportunities
				to marginalized people - we know that having a diverse workplace that values all voices equally
				benefits us all. we are also dedicated to working with individuals who are part of the
				communities we’re creating for because no one understands the needs of a community better
				than the people in that community. if you’re a creative professional from a marginalized
				community, we’d love to hear from you! hit us up here.
			</p>
		</div>
		<div class="sub-cont">
			<Block {...values[3]}/>
			<p>
				we aim to make our services available to all people, specifically populations that are often
				excluded from receiving high-quality creative work. we offer a sliding scale option for
				business owners that are from the LTGTQIA+ community, Native communities, all
				communities of color, and/or anyone with a disability. if you belong to any of these
				communities, we would love to work with you to build a product that meets your needs
				without exceeding your means.
			</p>
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
	#values-cont{
		padding-left: 2rem;
	}
	.sub-cont{
		display:grid;
	}
	p{
		align-self: center;
		justify-self: center;
		margin-top:0;
		max-width:80%;
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

	@media screen and (min-width:800px){
		p{
			font-size: 1.2rem;
			max-width:100%;
		}
	}
</style>