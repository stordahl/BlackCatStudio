<svelte:head>
	<title>Black Cat Studio: Our Team</title>
</svelte:head>

<script>
	import Member from '../components/Member.svelte'
	import Form from '../components/MainForm.svelte';


	const members = [
		{
			name: 'Jacob Stordahl',
			pronouns: 'he/him',
			desc: 'Jacob spent the beginning of his career working as a welder/fabricator where he gained experience solving complex problems. Now as a front-end developer, Jacob is very passionate about helping business owners create digital solutions that accomplish their goals',
			image: '/nick.jpg',
			alt: ''
		},
		{
			name: 'Nick Quandt',
			pronouns: 'he/him',
			desc: 'Jacob spent the beginning of his career working as a welder/fabricator where he gained experience solving complex problems. Now as a front-end developer, Jacob is very passionate about helping business owners create digital solutions that accomplish their goals',
			image: '/nick.jpg',
			alt: ''
		},
		{
			name: 'Taelor Hill',
			pronouns: 'they/them',
			desc: 'Jacob spent the beginning of his career working as a welder/fabricator where he gained experience solving complex problems. Now as a front-end developer, Jacob is very passionate about helping business owners create digital solutions that accomplish their goals',
			image: '/nick.jpg',
			alt: ''
		}
	];
</script>


<div id="content">
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