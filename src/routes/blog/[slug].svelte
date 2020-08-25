<svelte:head>
	<title>Black Cat Studio | {post.title}</title>
</svelte:head>

<script context="module">
	export async function preload({ params, query }) {
		// the `slug` parameter is available because
		// this file is called [slug].svelte
		const res = await this.fetch(`blog/${params.slug}.json`);
		const data = await res.json();

		if (res.status === 200) {
			return { post: data };
		} else {
			this.error(res.status, data.message);
		}
	}
</script>

<script>
	import Arrow from '../../components/Arrow.svelte';
	export let post;

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

<Arrow />
<div class="post-heading" style="--hover-color: {color}">
	<h1>{post.title}</h1>
	<a href="/blog" id="back-link">back</a>
</div>

<div class='content'>
	{@html post.html}
</div>

<style>
	/*
		By default, CSS is locally scoped to the component,
		and any unused styles are dead-code-eliminated.
		In this page, Svelte can't know which elements are
		going to appear inside the {{{post.html}}} block,
		so we have to use the :global(...) modifier to target
		all elements inside .content
	*/
	.content :global(h2) {
		font-size: 1.4em;
		font-weight: 500;
	}
	.content :global(img){
		max-width:100%;
		margin:2rem 0;
	}

	.content :global(pre) {
		background-color: #f9f9f9;
		box-shadow: inset 1px 1px 5px rgba(0,0,0,0.05);
		padding: 0.5em;
		border-radius: 2px;
		overflow-x: auto;
	}

	.content :global(pre) :global(code) {
		background-color: transparent;
		padding: 0;
	}

	.content :global(ul) {
		line-height: 1.5;
	}

	.content :global(li) {
		margin: 0 0 0.5em 0;
	}
	.content{
		/* width:60vw; */
		justify-self: center;
	}
	.post-heading{
		width:100%;
		display:flex;
		justify-content: space-between;
		justify-self: center;
	}
	#back-link{
		width: max-content;
		padding-bottom: 10px;
	}
	#back-link:hover{
		background-image: linear-gradient(transparent 80%, var(--hover-color) 20%);
		background-size: 124px 34px;
		padding-bottom: 10px;
		transition: all .7s ease;
	}
	@media screen and (min-width:900px){
		.content{
			width:60vw;
		}
		.post-heading{
			width:60vw;
		}
	}
</style>