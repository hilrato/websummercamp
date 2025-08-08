<script>
	import Button from '../../components/Button.svelte';
</script>

<div class="w-full bg-yellow-100">
	<div class="prose p-5">
		<h1 class="text-center">Simba's Profile</h1>

		<hr />

		<div
			class="profile-image h-20 w-20 overflow-hidden rounded-full bg-black bg-cover bg-center"
		></div>
		<div>Simba</div>
		<div>Lionhead Rabbit</div>

		<h2>About Me</h2>
		<p>Hi, my name is Simba the Lionhead Rabbit.</p>

		<h2>Haiku Exercise</h2>
		<div class="m-2 rounded-lg bg-white p-1">
			<div class="m-2 bg-blue-200 p-1 text-center text-blue-700">Sands of time slipping.</div>
			<div class="m-2 bg-green-200 p-1 text-center text-green-700">
				Through fingers, some people live.
			</div>
			<div class="m-2 bg-pink-200 p-1 text-center text-pink-700">Many just exist.</div>
		</div>

		<h2>Components</h2>

		<Button text={'Click Me'} message={'I am clicked'} animation={'pulse'} />
		<Button text={'Dont Click Me'} message={'Why did you click me?'} animation={'spin'} />
		<Button text={'More Info'} animation={'bounce'} />
	</div>
</div>

<style>
	.profile-image {
		background-image: url('https://media.istockphoto.com/id/1468320713/photo/cute-white-rabbit-on-grass-looking-straight.webp?a=1&b=1&s=612x612&w=0&k=20&c=a7sW_TzGiMu5pX1l5PJoJK58qWxPxk42tlNvuYZ8yho=');
	}
</style>
