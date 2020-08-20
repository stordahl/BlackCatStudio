<svelte:head>
	<title>Black Cat Studio: Blog</title>
</svelte:head>

<script context="module">
	
	export function preload({ params, query }) {
		return this.fetch(`blog.json`).then(r => r.json()).then(posts => {
			return { posts };
		});
	}
	
</script>

<script>
 	import Arrow from '../../components/Arrow.svelte';
	export let posts;

	// let shapes = [];
	// let rnd = shapes[Math.floor(Math.random()*shapes.length)];

	const colors = [
		'#DDA788',
		'#BB5215',
		'#E6F2FF',
		'#A5C4E7',
		'#999E90',
		'#4E563E',
	];

	let color = colors[Math.floor(Math.random() * colors.length)];
</script>

<style>
	ul {
		margin: 0 0 1em 0;
		line-height: 2;
		list-style: none;
	}
	a{
		width: max-content;
		padding-bottom: 10px;
	}
	a:hover{
		background-image: linear-gradient(transparent 70%, var(--hover-color) 30%);
		background-size: 60px 52px;
		transition: all .7s ease;
	}
	a{
		font-size:2rem;
		text-transform: lowercase;
	}
	h5{
		font-size:1.1rem;
		opacity:60%;
		font-weight:600;
		letter-spacing: 3px;
		text-align: right;
	}
	.headline{
		margin:0 1rem;
		margin-bottom:2rem;
		width:100%;
		display:flex;
		flex-direction:column;
		align-items: flex-end;
	}
</style>

<!-- uncomment when post list exceeds desktop vh -->
<!-- <Arrow /> -->

<div class="headline">
	<h5>this blog is a collection of information we feel is</h5>
	<h5>important or valuable to our clients & stakeholders.</h5>
</div>

<ul style="--hover-color: {color}">
	{#each posts as post}
		<!-- we're using the non-standard `rel=prefetch` attribute to
				tell Sapper to load the data for the page as soon as
				the user hovers over the link or taps it, instead of
				waiting for the 'click' event -->
		<li><a rel='prefetch' href='blog/{post.slug}'>{post.title}</a></li>
	{/each}
</ul>
<!-- <img src="{ rnd }" alt="a background illustration"> -->