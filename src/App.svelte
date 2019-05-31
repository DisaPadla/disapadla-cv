<script>
	import Header from './Header.svelte';
	import Card from './Card.svelte';
	import Details from './Details.svelte';
	import templates from './template.js';
</script>

<style>
	div {
		position: relative;
		padding: 80px 20px 20px 20px;
		display: flex;
    flex-direction: column;
		align-items: center;
		min-height: 100%;
		background: #252827;
		background-image: linear-gradient(0deg, transparent 24%,
			rgba(255, 255, 255, .05) 25%,
			rgba(255, 255, 255, .05) 26%, transparent 27%, transparent 74%, 
			rgba(255, 255, 255, .05) 75%, 
			rgba(255, 255, 255, .05) 76%, transparent 77%, transparent
		),
		linear-gradient(90deg, transparent 24%, 
			rgba(255, 255, 255, .05) 25%, 
			rgba(255, 255, 255, .05) 26%, transparent 27%, transparent 74%, 
			rgba(255, 255, 255, .05) 75%, 
			rgba(255, 255, 255, .05) 76%, transparent 77%, transparent
		);
		background-size:20px 20px;
		
	}
	article {
		border-left: 2px solid #D6DFE0;
	}

	span {
		position: relative;
		bottom: 0;
		margin-top: 40px;
		font-size: 12px;
		text-align: center;
	}

	a {
		color: #C7F954;
    text-shadow: 0 0 2px #393a33, 0 0 35px #ffffff44, 0 0 8px #f39f0575, 0 0 2px #f39f0575;
	}
</style>

<Header/>
<div>
	<article>
		{#each templates as template}
			<Card {...template}/>
		{/each}
	</article>
	<Details />
	<span
		title='I have an alarm which reminds me to stay asleep'
	>Created for fun. Powered by <a href='https://svelte.dev' target="_blank">Svelte</a></span>
</div>
