<div class="p-5 text-center text-4xl font-bold">FLEX</div>

<!-- Flex has to be applied to parent 
 Justify content
 - center
 - start
 - end
 - between -->

<!-- Align Items
  - center -->

<!-- Flexbox Froggy -->
<div class="flex h-20 items-center justify-center border bg-yellow-100">
	<div class="h-10 w-10 rounded border"></div>
	<div class="h-10 w-10 rounded border"></div>
	<div class="h-10 w-10 rounded border"></div>
	<div class="h-10 w-10 rounded border"></div>
</div>

<div class="flex h-50 flex-col items-center justify-center border bg-pink-100">
	<div class="h-10 w-10 rounded border"></div>
	<div class="h-10 w-10 rounded border"></div>
	<div class="h-10 w-10 rounded border"></div>
	<div class="h-10 w-10 rounded border"></div>
</div>

<div class="flex">
	<div class="m-5 flex h-50 w-50 items-end justify-center border">
		<div class="h-10 w-10 border bg-blue-100"></div>
		<div class="h-10 w-10 border bg-blue-100"></div>
		<div class="h-10 w-10 border bg-blue-100"></div>
		<div class="h-10 w-10 border bg-blue-100"></div>
	</div>

	<div class="m-5 flex h-50 w-50 flex-col items-center justify-between border">
		<div class="h-10 w-10 border bg-blue-100"></div>
		<div class="h-10 w-10 border bg-blue-100"></div>
		<div class="h-10 w-10 border bg-blue-100"></div>
		<div class="h-10 w-10 border bg-blue-100"></div>
	</div>

	<div class="m-5 flex h-50 w-50 items-start justify-end border">
		<div class="h-10 w-10 border bg-blue-100"></div>
		<div class="h-10 w-10 border bg-blue-100"></div>
		<div class="h-10 w-10 border bg-blue-100"></div>
		<div class="h-10 w-10 border bg-blue-100"></div>
	</div>

	<div class="m-5 flex h-50 w-50 items-end justify-between border">
		<div class="h-10 w-10 border bg-blue-100"></div>
		<div class="h-10 w-10 border bg-blue-100"></div>
		<div class="h-10 w-10 border bg-blue-100"></div>
		<div class="h-10 w-10 border bg-blue-100"></div>
	</div>
</div>

<div class="m-5 flex h-50 w-50 flex-wrap content-start justify-end border">
	<div class="box bg-red-500"></div>
	<div class="box bg-green-500"></div>
	<div class="box bg-blue-500"></div>
	<div class="box bg-yellow-500"></div>
</div>

<div class="m-5 flex h-50 w-50 flex-wrap content-between items-start justify-end border">
	<div class="box bg-red-500"></div>
	<div class="box bg-green-500"></div>
	<div class="box bg-blue-500"></div>
	<div class="box bg-yellow-500"></div>
</div>

<div class="m-5 flex h-50 w-50 flex-wrap items-center justify-between border">
	<div class="box bg-red-500"></div>
	<div class="box bg-green-500"></div>
	<div class="box bg-blue-500"></div>
	<div class="box bg-yellow-500"></div>
</div>

<div class="m-5 flex h-50 w-50 flex-wrap content-center items-center justify-center border">
	<div class="box bg-red-500"></div>
	<div class="box bg-green-500"></div>
	<div class="box bg-blue-500"></div>
	<div class="box bg-yellow-500"></div>
</div>

<style>
	.box {
		height: 40%;
		width: 40%;
	}
</style>
