<!-- Horse.svelte -->
<script>
	let { emote, position, color, animation } = $props();
</script>

<div class="m-3 flex h-15 items-center bg-gray-200">
	<div style="width:{position}%" class="h-full shrink-0 transition-all duration-1000 {color}"></div>
	<div class="animal {animation}">{emote}</div>
</div>

<style>
	.animal {
		font-size: 45px;
	}

	.bounce {
		animation: bounce 0.5s infinite;
	}

	.spin {
		animation: spin 0.5s infinite;
	}

	.pulse {
		animation: pulse 1s cubic-bezier(0.8, 0.8, 0.6, 1) infinite;
	}
</style>
