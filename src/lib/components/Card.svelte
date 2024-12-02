<script>
	import Modal from './Modal.svelte';
	const { calenderNumber, cardImage, cardText, isClickable } = $props();
	let showModal = $state(false);

	function openModal() {
		if (!isClickable) {
			return;
		}
		showModal = true;
	}
</script>

<Modal bind:showModal>
	{#if cardImage}
		<!-- svelte-ignore a11y_img_redundant_alt -->
		<img src={cardImage} alt="This is an image for the calendar item" />
	{/if}
	{#if cardText}
		<p class="modalText">{cardText}</p>
	{/if}
</Modal>
<!-- svelte-ignore a11y_click_events_have_key_events -->
<!-- svelte-ignore a11y_no_static_element_interactions -->
<!-- svelte-ignore event_directive_deprecated -->
<div on:click={() => openModal()} class:disabled={!isClickable}>
	<p>{calenderNumber}</p>
</div>

<style>
	img {
		max-width: 100%;
		max-height: 70vh;
		border-radius: 10px;
		object-fit: cover;
		margin: 0 auto;
		display: block;
		padding-bottom: 20px;
	}

	.modalText {
		font-size: 28px;
	}
	div {
		width: 200px;
		height: 200px;
		border-radius: 10px 10px 10px 10px;
		text-align: center;
		display: flex;
		align-items: center;
		justify-content: center;
		background-color: white;
		&:hover {
			cursor: pointer;
			background-color: #eee;
		}

		p {
			font-size: 80px;
			color: rgb(13, 46, 13);
		}
	}

	.disabled {
		background-color: #aaa; /* Greyed-out for disabled days */
		cursor: not-allowed;
		&:hover {
			cursor: not-allowed;
			background-color: #aaa;
		}
	}
</style>
