<script>
	import { onMount } from 'svelte';
	import Button from '../../components/Button.svelte';

	let points = $state(0);
	let clickingPower = $state(1);
	let passiveIncome = $state(1);

	let upgradeClickCost = 100;
	let upgradePassiveCost = 500;

	onMount(() => {
		// INTERVAL
		let passiveTimer = setInterval(() => {
			points += passiveIncome;
		}, 1000);

		return () => clearInterval(passiveTimer);
	});

	function increment() {
		// make a button that increases seconds by 1
		points += clickingPower;
	}

	function upgradeClickingPower(amount) {
		if (points - amount * upgradeClickCost >= 0) {
			points -= amount * upgradeClickCost;
			clickingPower += amount;
		}
	}

	function upgradePassiveIncome(amount) {
		if (points - amount * upgradePassiveCost >= 0) {
			points -= amount * upgradePassiveCost;
			passiveIncome += amount;
		}
	}
</script>

<!-- container for game -->
<div class="flex h-screen flex-col items-center justify-center bg-blue-200">
	<div class="p-2">{points}</div>
	<!-- svelte-ignore a11y_consider_explicit_label -->
	<button
		onclick={increment}
		class="h-48 w-48 rounded-full bg-gradient-to-br from-pink-500 via-pink-300 to-pink-500 transition-all duration-250 active:scale-110"
	></button>
</div>

<div class="flex w-full border">
	<div class="w-1/2">
		<div>Click Upgrades</div>
		<Button text="+1 - {1 * upgradeClickCost}" fn={() => upgradeClickingPower(1)} />
		<Button text="+5 - {5 * upgradeClickCost}" fn={() => upgradeClickingPower(5)} />
	</div>
	<div class="w-1/2">
		<div>Passive Upgrades</div>
		<Button text="+1 - {1 * upgradePassiveCost}" fn={() => upgradePassiveIncome(1)} />
	</div>
</div>

<!-- <Button text={'+1'} fn={increment} /> -->
