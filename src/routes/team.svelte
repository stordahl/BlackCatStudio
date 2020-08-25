<svelte:head>
	<title>Black Cat Studio: Our Team</title>
</svelte:head>

<script>
	import Member from '../components/Member.svelte';
	import Form from '../components/MainForm.svelte';
	import Arrow from '../components/Arrow.svelte';


	const members = [
		{
			name: "Jacob Stordahl",
			pronouns: "he/him",
			desc: "Jake is a front-end developer, who is deeply passionate about building intuitive User Interfaces using Javascript, HTML, and CSS. His main goal in creating BCS is to help small businesses make their creative goals a tangible reality using digital technologies. When Jake isn't writing code he's probably cruising on his roller skates or cuddling his two kittens. ",
			image: "/jake.jpg"
		},
		{
			name: "Nick Quandt",
			pronouns: "he/him",
			desc: "Nick is a software engineer with a passion for writing scalable solutions in Javascript, TypeScript, and Node.js. Seattle dog dad & outdoor enthusiast. Ask me anything about programming, data, bbq, or cowboy boots!",
			image: "/nick.jpg"
		},
		{
			name: "Taelor Hill",
			pronouns: "they/them",
			desc: "Taelor is an illustrator and graphic designer, focusing primarily in creating and sharing educational content digitally. Their passions include using social media as a vehicle for social change, supporting marginalized communities, and using art as a form of activism. You can usually find them playing with their cats, worrying about all their plants, or baking something sweet.",
			image: "/tae.jpg"
		}
	];
</script>

<Arrow />
<div id="content">
	<h1>meet our team!</h1>
		<Member {...members[0]}/>
		<Member {...members[1]}/>
		<Member {...members[2]}/>
		<hr>
		<Form />
</div>

<style>
	#content{
		display:grid
	}
	hr{
		width:100%;
		max-width:70%;
		justify-self:center;
		margin-bottom:4rem;
	}
</style>