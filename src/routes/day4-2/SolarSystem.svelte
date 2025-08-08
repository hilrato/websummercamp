<div class="relative h-screen overflow-hidden bg-gradient-to-b from-black via-purple-900 to-black">
	<div
		class="centered h-8 w-8 rounded-full bg-gradient-to-b from-red-600 via-orange-600 to-red-500"
	></div>

	<!-- Mercury -->
	<div
		class="centered h-13 w-13 animate-[spin_12s_linear_infinite] rounded-full border border-gray-200/40"
	>
		<div class="absolute h-3 w-3 translate-0.5 rounded-full bg-blue-300"></div>
	</div>

	<!-- Venus -->
	<div
		class="centered h-18 w-18 animate-[spin_12s_linear_infinite] rounded-full border border-gray-200/40"
	>
		<div class="absolute h-3 w-3 translate-0.5 rounded-full bg-blue-300"></div>
	</div>

	<!-- earth -->
	<div
		class="centered h-28 w-28 animate-[spin_16s_linear_infinite] rounded-full border border-gray-200/40"
	>
		<div
			class="absolute h-4 w-4 translate-[8px] animate-[spin_5s_linear_infinite] rounded-full bg-gradient-to-b from-blue-300 via-green-600 to-green-700"
		>
			<div class="h-1 w-1 -translate-[5px] rounded-full bg-white"></div>
		</div>
	</div>

	<!-- Mars -->
	<div
		class="centered h-37 w-37 animate-[spin_12s_linear_infinite] rounded-full border border-gray-200/40"
	>
		<div class="absolute h-3 w-3 translate-[14px] rounded-full bg-blue-300"></div>
	</div>

	<!-- stars -->
	{#each Array(100) as _, i}
		<div
			class="absolute h-1 w-1 rounded-full bg-white/60"
			style="top: {Math.random() * 90}vh; left: {Math.random() *
				90}vw; animation-delay: {Math.floor(Math.random() * 250)}ms;"
		></div>
	{/each}
</div>

<style>
	.centered {
		@apply absolute top-1/2 left-1/2 -translate-1/2;
	}
</style>
