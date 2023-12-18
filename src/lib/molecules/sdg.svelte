<script>
	import SdgImage from '../atoms/sdgImage.svelte';
	export let data;
	// console.log(data.wish.image.url);
</script>

<section class="container-susDevGoal">
	<img
		class="susDevGoal"
		src="https://upload.wikimedia.org/wikipedia/commons/thumb/5/50/Sustainable_Development_Goal_01NoPoverty.svg/599px-Sustainable_Development_Goal_01NoPoverty.svg.png"
		alt="sustainable development goal 1"
	/>
	<SdgImage {data} />
</section>

<style>
	.susDevGoal {
		max-width: 100px;
		max-height: 100px;
		margin: 1em;
	}
	.container-susDevGoal {
		display: flex;
		flex-direction: row;
		margin-left: 2em;
	}
</style>
