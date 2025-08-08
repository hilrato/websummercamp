<script>
	let { text, fn } = $props();

	// function test() {
	// 	alert(message);
	// }
</script>

<button
	onclick={fn}
	class={`m-2 rounded border px-3 py-1 transition-all duration-1000 hover:animate-pulse hover:bg-black hover:text-white active:scale-130`}
	>{text}</button
>
