<script lang="ts">
	let paScore = 0;
	let quizScore = 0;
	let quarterlyScore = 0;
	let engagementScore = 0;

	$: totalPa = (paScore / 60) * 50;
	$: totalQuiz = (quizScore / 40) * 20;
	$: totalQuarterly = (quarterlyScore / 60) * 20;
	$: totalEngagement = (engagementScore / 10) * 10;

	$: total = totalPa + totalQuiz + totalQuarterly + totalEngagement;
</script>

<main>
	<h1 class="my-8 text-center text-8xl font-bold text-white">Galc</h1>
	<form class="flex flex-col items-center justify-center gap-4">
		<label class="text-2xl text-white" for="paScore">Performance Assessment Score</label>
		<input
			type="number"
			class="block rounded-md border-none bg-white px-4 py-2 text-xl outline-none"
			bind:value={paScore}
			id="paScore"
		/>
		<label class="text-2xl text-white" for="quizScore">Quiz Score</label>
		<input
			type="number"
			class="block rounded-md border-none bg-white px-4 py-2 text-xl outline-none"
			bind:value={quizScore}
			id="quizScore"
		/>
		<label class="text-2xl text-white" for="quarterlyScore">Quarterly Score</label>
		<input
			type="number"
			class="block rounded-md border-none bg-white px-4 py-2 text-xl outline-none"
			bind:value={quarterlyScore}
			id="quarterlyScore"
		/>
		<label class="text-2xl text-white" for="paScore">Engagement Score</label>
		<input
			type="number"
			class="block rounded-md border-none bg-white px-4 py-2 text-xl outline-none"
			bind:value={engagementScore}
			id="engagementScore"
		/>
	</form>
	<p class="my-4 text-center text-4xl text-white">Total: {total}</p>
</main>

<p class="text-center text-white">Made with 🔥 by Iño</p>
