<script>
	import adventfox from '$lib/images/adventfox.jpg';
	import joker from '$lib/images/joker.jpeg';
	import aprillludgate from '$lib/images/aprilludgate.webp';
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
			text: `"The only things I like are dogs, sleeping late, and weird birthmarks. You can’t make museums about those." - April Ludgate"`
		},
		{
			day: 4,
			image: adventfox,
			text: undefined
		},
		{
			day: 5,
			image: undefined,
			text: 'quote here'
		},
		{
			day: 6,
			image: undefined,
			text: 'quote here'
		},
		{
			day: 7,
			image: undefined,
			text: 'quote here'
		},
		{
			day: 8,
			image: undefined,
			text: 'quote here'
		},
		{
			day: 9,
			image: undefined,
			text: 'quote here'
		},
		{
			day: 10,
			image: undefined,
			text: 'quote here'
		},
		{
			day: 11,
			image: undefined,
			text: 'quote here'
		},
		{
			day: 12,
			image: undefined,
			text: 'quote here'
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
