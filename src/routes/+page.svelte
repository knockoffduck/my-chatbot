<script>
	import TextArea from '../components/TextArea.svelte';
	import ChatNav from '../components/ChatNav.svelte';
	import PromptNav from '../components/PromptNav.svelte';
	import ChatSetup from '../components/ChatSetup.svelte';

	let showLeftSidebar = true;
	let showRightSidebar = true;
</script>

<div class="bg-surface-500 w-screen h-screen flex justify-between overflow-hidden">
	{#if showLeftSidebar}
		<ChatNav />
	{/if}
	<main class="h-full w-full flex flex-col p-2">
		<nav class="flex w-full justify-between">
			<button class="btn p-0" on:click={() => (showLeftSidebar = showLeftSidebar ? false : true)}>
				<svg
					xmlns="http://www.w3.org/2000/svg"
					fill="none"
					viewBox="0 0 24 24"
					stroke-width="1.5"
					stroke="currentColor"
					class="w-6 h-6"
				>
					<path stroke-linecap="round" stroke-linejoin="round" d="M15.75 19.5L8.25 12l7.5-7.5" />
				</svg>
			</button>

			<button class="btn p-0" on:click={() => (showRightSidebar = showRightSidebar ? false : true)}>
				<svg
					xmlns="http://www.w3.org/2000/svg"
					fill="none"
					viewBox="0 0 24 24"
					stroke-width="1.5"
					stroke="currentColor"
					class="w-6 h-6"
				>
					<path stroke-linecap="round" stroke-linejoin="round" d="M8.25 4.5l7.5 7.5-7.5 7.5" />
				</svg>
			</button>
		</nav>
		<div class="m-6 ml-64 mr-64 flex flex-col items-center gap-5 h-full justify-between">
			<ChatSetup />
			<div class="flex flex-col w-full gap-4 items-center">
				<button class="btn variant-ghost rounded-md w-fit">Regenerate Response</button>
				<div class="w-full flex gap-2">
					<TextArea />
				</div>
			</div>
		</div>
	</main>
	{#if showRightSidebar}
		<PromptNav />
	{/if}
</div>
