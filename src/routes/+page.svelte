<script>
	import adventfox from '$lib/images/adventfox.jpg';
	import adventfox2 from '$lib/images/adventfox2.jpg';
	import joker from '$lib/images/joker.jpeg';
	import aprillludgate from '$lib/images/aprilludgate.webp';
	import lizard from '$lib/images/lizard.png';
	import foxandraccoon from '$lib/images/foxandraccoon.jpg';
	import friesiangif from '$lib/images/friesiangif.gif';
	import hquinngif from '$lib/images/hquinn.gif';
	import howdygif from '$lib/images/howdygif.gif';
	import reindeer from '$lib/images/reindeer.jpg';

	import Card from '$lib/components/Card.svelte';

	const today = new Date().getDate();

	const calendarItems = [
		{
			day: 1,
			image: adventfox,
			text: undefined
		},
		{
			day: 2,
			image: joker,
			text: `"I believe whatever doesn't kill you makes you. . . stranger," - Joker`
		},
		{
			day: 3,
			image: aprillludgate,
			text: `"The only things I like are dogs, sleeping late, and weird birthmarks. You can’t make museums about those." - April Ludgate`
		},
		{
			day: 4,
			image: adventfox2,
			text: ''
		},
		{
			day: 5,
			image: lizard,
			text: `DID YOU KNOW the New Mexican Whiptail is a female-only species of lizard? They reproduce asexually. They are otherwise wary, energetic, and fast moving. Lesbian lizards FTW!`,
			cardLink: 'https://www.youtube.com/watch?v=3WqU9wCKVRI',
			cardLinkText: `Check 'em out!'`
		},
		{
			day: 6,
			image: 'https://i.pinimg.com/originals/07/66/a1/0766a14d9320aa1a4942875e224a0e9d.gif',
			cardLink: 'https://www.youtube.com/watch?v=5gZrYyi-XRQ',
			cardLinkText: 'Once Upon a December'
		},
		{
			day: 7,
			image: 'https://y.yarn.co/9b8d0e9f-f475-401b-8219-7ed6913b3274_text.gif',
			text: `"Now, this whole thing stinks three ways to Sunday!""`,
			cardLink: 'https://www.youtube.com/watch?v=Ig9vELiBnBs',
			cardLinkText: 'Watch Rango Scene'
		},
		{
			day: 8,
			image: foxandraccoon,
			text: ''
		},
		{
			day: 9,
			image: friesiangif,
			text: '',
			cardLink: 'https://www.youtube.com/watch?v=ReeKcqcLj0c&t=145s',
			cardLinkText: 'A documentary on Friesians 🐎'
		},
		{
			day: 10,
			image: hquinngif,
			text: `"Love your perfume. What is that, the scent of death?"`
		},
		{
			day: 11,
			image: howdygif,
			text: 'Honestly, the best part of the first movie right there.',
			cardLinkText: "You've got a friend in me",
			cardLink: 'https://www.youtube.com/watch?v=0hG-2tQtdlE'
		},
		{
			day: 12,
			image: reindeer,
			text: 'DID YOU KNOW that reindeer have eyes that turn blue in the winter? It is to help them see in lower light levels. They are golden colored in the summer. No other mammals have this ability. They are also the only deer species in which both the male and female can grow antlers. Also, they do actually have red noses with lots of tiny veins circulating warm blood around their nose to heat up the air they breathe so they do not get too cold.'
		},
		{
			day: 13,
			image: undefined,
			text: 'quote here'
		},
		{
			day: 14,
			image: undefined,
			text: 'quote here'
		},
		{
			day: 15,
			image: undefined,
			text: 'quote here'
		},
		{
			day: 16,
			image: undefined,
			text: 'quote here'
		},
		{
			day: 17,
			image: undefined,
			text: 'quote here'
		},
		{
			day: 18,
			image: undefined,
			text: 'quote here'
		},
		{
			day: 19,
			image: undefined,
			text: 'quote here'
		},
		{
			day: 20,
			image: undefined,
			text: 'quote here'
		},
		{
			day: 21,
			image: undefined,
			text: 'quote here'
		},
		{
			day: 22,
			image: undefined,
			text: 'quote here'
		},
		{
			day: 23,
			image: undefined,
			text: 'quote here'
		},
		{
			day: 24,
			image: undefined,
			text: 'quote here'
		},
		{
			day: 25,
			image: undefined,
			text: 'quote here'
		},
		{
			day: 26,
			image: undefined,
			text: 'quote here'
		},
		{
			day: 27,
			image: undefined,
			text: 'quote here'
		},
		{
			day: 28,
			image: undefined,
			text: 'quote here'
		},
		{
			day: 29,
			image: undefined,
			text: 'quote here'
		},
		{
			day: 30,
			image: undefined,
			text: 'quote here'
		},
		{
			day: 31,
			image: adventfox,
			text: undefined
		}
	];
</script>

<svelte:head>
	<title>Advent Calendar</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section>
	<h1>Harley's Advent Calendar 🎄</h1>
	<div class="calendarContainer">
		{#each calendarItems as items}
			<Card
				calenderNumber={items.day}
				cardText={items.text}
				cardImage={items.image}
				isClickable={items.day <= today}
				cardLink={items.cardLink}
				cardLinkText={items.cardLinkText}
			/>
		{/each}
	</div>
</section>

<style>
	h1 {
		font-weight: 400;
		font-size: 18px;
		color: #eee;
		text-align: center;

		@media (min-width: 360px) {
			font-size: 32px;
		}
		@media (min-width: 800px) {
			font-size: 32px;
		}
	}
	section {
		display: flex;
		flex-direction: column;
		align-items: center;
		gap: 20px;
		margin: 0 50px;
	}
	.calendarContainer {
		display: grid;
		gap: 15px;
		grid-template-columns: repeat(2, 1fr);

		@media (min-width: 900px) {
			grid-template-columns: repeat(4, 1fr);
		}

		@media (min-width: 1500px) {
			grid-template-columns: repeat(7, 1fr);
		}
	}
</style>
