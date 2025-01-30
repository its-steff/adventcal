<script>
</script>

<svelte:head>
	<title>4e Character Builder</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section>
	<h1>Character Builder WIP</h1>
	<div class="calendarContainer"></div>
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
