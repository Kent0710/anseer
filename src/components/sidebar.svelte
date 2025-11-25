<script lang="ts">
	import { twMerge } from 'tailwind-merge';
	import { Home } from '@lucide/svelte';

	export let _class: string = '';

	const navs = [{ name: 'Home', icon: Home, href: '/home' }];
</script>

<div
	class={twMerge(
		'rounded-full relative overflow-hidden bg-gradient-to-b from-blue-500 to-pink-500 border-white',
		_class
	)}
>
	<!-- Parent Frosted Glass -->
	<div class="absolute inset-0 bg-white/20 backdrop-blur-xl z-10 pointer-events-none"></div>

	<!-- Content -->
	<ul class="relative z-20 flex justify-center gap-6 py-6">
		{#each navs as nav}
			<li class="relative overflow-hidden rounded-full  p-4 flex flex-col items-center">
				<!-- Frosted glass inside li -->
				<div class="absolute inset-0 bg-white/20 rounded-full border-white border-1 backdrop-blur-lg z-0 pointer-events-none"></div>

				<!-- Content -->
				<a
					href={nav.href}
					class="relative z-10 flex flex-col items-center text-neutral-200 hover:text-white"
				>
					<svelte:component this={nav.icon} />
				</a>
			</li>
		{/each}
	</ul>
</div>
