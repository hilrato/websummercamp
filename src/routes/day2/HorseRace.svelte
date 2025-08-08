<script>
	import Horse from './Horse.svelte';
	import Button from '../../components/Button.svelte';

	//array of horses
	let horses = $state([
		{
			emote: '🏃‍➡️',
			position: 5,
			color: 'bg-gradient-to-r from-blue-200 via-blue-400 to-blue-600',
			animation: 'bounce'
		},

		{
			emote: '🏃🏼‍♂️‍➡️',
			position: 5,
			color: 'bg-gradient-to-r from-green-200 via-green-400 to-green-600',
			animation: 'bounce'
		},

		{
			emote: '🏃🏻‍♀️‍➡️',
			position: 5,
			color: 'bg-gradient-to-r from-pink-200 via-pink-400 to-pink-600',
			animation: 'bounce'
		}
	]);

	function progress() {
		let maxHorse = horses[0];
		for (let horse of horses) {
			let r = parseInt(Math.random() * 20);
			horse.position += r;
			if (horse.position > 100) {
				horse.position = 100;
			}

			if (horse.position > maxHorse.position) {
				maxHorse = horse;
			}
		}
		for (let horse of horses) {
			if (horse.position == maxHorse.position) {
				horse.animation = 'spin';
			} else {
				horse.animation = 'bounce';
			}
		}
	}
</script>

<div style="height: 400px;" class="bg-gray-600">
	<div class="py-5 text-center text-2xl font-bold">Who Will Win?</div>
	<Button text={'Let Them Run'} fn={progress} />
	<div class="pr-10">
		{#each horses as horse}
			<Horse
				emote={horse.emote}
				color={horse.color}
				animation={horse.animation}
				position={horse.position}
			/>
		{/each}
	</div>
</div>
