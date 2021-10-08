<script lang="ts">
	import { tw, apply } from 'twind';

	const btn = apply`inline-block bg-gray-500 text-white text-base rounded px-4 py-2`;
	const h1 = apply`font-bold text(center 5xl white sm:gray-800 md:pink-700)`;
	const p = tw`bg-gray-200 ${false && 'rounded'}`
	const isTrue = true
	const obj =tw({ 'bg-yellow-200': true, rounded: false, underline: isTrue })
	const array =tw(['bg-green-200'], ['', 0, false, 'rounded'], [['underline']])
</script>

<svelte:head>
	<title>Home</title>
</svelte:head>

<section class="${tw`h-screen text-center my-4 mx-4`}">
	<h1 class={tw`${h1}`}>This is Twind!</h1>
	<button class={tw`${btn}`}>Twind Button</button>
	<p class={p}>emplate Literal (recommended)</p>
	<p class={obj}>Objects</p>
	<p class={array}>Array</p>
</section>
