<script>
	import { onMount } from 'svelte';
	import { src_url_equal } from 'svelte/internal';
	let fortune = '';
	let name = '';

	function getFortune() {
		// do whatever you want
		console.log('Hello');
		let fortunes = [
			'Every good and perfect gift is from above.',
			'The grass is always greener on the other side.',
			'Little by little, one travels far.',
			'You will die alone and poorly dressed.',
			"A fanatic is one who can't change his mind, and won't change the subject.",
			'If you look back, you’ll soon be going that way.',
			'You will live long enough to have aliens abduct you.',
			'An alien of some sort will be appearing to you shortly.',
			'Do not mistake temptation for opportunity.',
			'Flattery will go far tonight.',
			'Lose weight or you will be depressed.',
			'Some dream of fortunes but I think you dream of cookies',
			'The greatest danger could be your stupidity.',
			'We don’t know the future, only you do.',
			"The world may be your oyster, but it doesn't mean you'll get its pearl.",
			'You will be hungry in the next hour.',
			'The road to riches is paved with homework.',
			'You can always find happiness at work on Friday.',
			'I was waiting for the algorithm to choose me. I am free at last!',
			"Don't behave with cold manners.",
			'Don’t forget you are always on our minds.',
			'Fortune not found? Abort, Retry, Ignore.',
			'Never forget a friend. Especially if they owe you.',
			'It is a good day to have a good day.',
			'Yo hablo espanol. Que tengas un buen dia.',
			'Zoodini is tired darling, try again later.',
			'Zpv tvdl. Decode it.', "Your car will be scatched.", "The grass isn't greener", "You are loved."
		];
		console.log(fortunes);
		let i = Math.round(Math.random() * (fortunes.length - 1));
		console.log(fortunes[i]);
		fortune = fortunes[i];
	}
</script>

<h1 class="text">Greetings {name}! I am Zoodini from Niverkasing Tops.</h1>
<!-- svelte-ignore a11y-missing-attribute -->
<img src="/paper_fortune.png" />

<br />
<input bind:value={name} placeholder="Enter your name" />
<button class="text" on:click={getFortune}> Get Fortune </button>
<h2 class="text">CLICK IF YOU DARE!</h2>
<h2 class="text">{fortune}</h2>

<style>
	input,
	button {
		display: block;
		margin: auto;
		margin-top: 20px;
	}
	input {
		padding: 10px;
	}
	button {
		font-size: large;
		padding: 20px;
	}
	.text {
		font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
		font-size: 3rem;
		color: rgb(45, 45, 49);
		text-align: center;
	}
	img {
		height: 200px;
		width: center;
		display: block;
		margin: auto;
		margin-top: 50px;
	}
	:global(body) {
		background-color: rgb(212, 130, 130);
	}
</style>
