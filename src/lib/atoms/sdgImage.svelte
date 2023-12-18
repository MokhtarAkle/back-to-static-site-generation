<script>
	export let data;

	// console.log(data);
</script>

<img class="susDevGoal" src={data.wish.image.image.url} alt="Sustainable development goals" />

<style>
	.susDevGoal {
		max-width: 100px;
		max-height: 100px;
		margin: 1em;
	}
</style>
