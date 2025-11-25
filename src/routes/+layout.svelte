<script lang="ts">
	import './layout.css';
	import favicon from '$lib/assets/favicon.svg';
	import Sidebar from '../components/sidebar.svelte';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

<div class="h-dvh w-dvw flex p-4">
	<Sidebar _class="w-[6rem]" />
	<main class="flex-1 overflow-hidden py-8 px-16">
		{@render children()}
	</main>
</div>
