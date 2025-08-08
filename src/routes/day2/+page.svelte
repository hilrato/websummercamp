<script>
	import Button from '../../components/Button.svelte';
	import LoadingBar from '../../components/LoadingBar.svelte';
	import HorseRace from './HorseRace.svelte';

	let progress = $state(10);

	function increment() {
		progress += 10;
		if (progress > 100) {
			progress = 100;
		}
	}

	//make different function with a button along with it
	function decrement() {
		progress -= 10;
		if (progress < 0) {
			progress = 0;
		}
	}

	//make a reset function that resets progress to 0
	function reset() {
		progress = 0;
	}
</script>

<!-- <button onclick={increment}>Increment</button>
<button onclick={decrement}>Decrement</button>
<button onclick={reset}>Reset</button> -->

<HorseRace />

<LoadingBar color={'bg-blue-500'} current={progress} max={100} />

<Button text={'Increment'} fn={increment} />
<Button text={'Decrement'} fn={decrement} />
<Button text={'Reset'} fn={reset} />

<div class="bg-red-500 text-center transition-all duration-1000 hover:bg-blue-500 hover:text-left">
	Transition
</div>

<div
	class="hover:text-uppercase m-2 w-15 border py-5 transition-all duration-1000 hover:mt-5 hover:w-30 hover:animate-bounce hover:rounded hover:border-red-500 hover:bg-pink-100 hover:text-center"
>
	Box 1
</div>
<div
	class="m-2 h-10 w-15 border transition-all duration-1000 hover:w-30 hover:animate-spin hover:rounded-l"
>
	Box 2
</div>
<div class="m-2 h-10 w-15 border transition-all duration-1000 hover:bg-green-100">Box 3</div>
<div
	class="m-2 w-15 border py-5 transition-all duration-1000 hover:w-30 hover:rounded-full hover:border-dotted hover:bg-yellow-200 hover:text-right"
>
	Box 4
</div>
<div
	class="m-2 h-10 w-15 border transition-all duration-1000 hover:translate-x-96 hover:rotate-700"
>
	Box 5
</div>
<div class="m-2 h-10 w-15 border transition-all duration-1000 hover:scale-150">Box 6</div>
