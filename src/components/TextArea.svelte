<script>
	let textarea;
	let lines = 1;

	const calculateLines = () => {
		lines = textarea.value.split('\n').length + 1;
		console.log(lines);
	};
</script>

<div
	class="flex items-center h-fit w-full text-left rounded-lg bg-transparent border px-4 py-2 focus-within:border-white text-neutral-900 border-neutral-600 dark:text-neutral-100"
>
	<textarea
		bind:this={textarea}
		class="bg-transparent outline-none w-full"
		placeholder="Enter a prompt or type &quot;/&quot; to select a prompt..."
		on:input={calculateLines}
		style="height: {lines}em; resize: none; max-height: 300px; min-height:2em; bottom: 64px;"
	/>
	<button class="btn variant-outline p-2 rounded-md h-fit variant-soft-surface"
		><svg
			xmlns="http://www.w3.org/2000/svg"
			fill="none"
			viewBox="0 0 24 24"
			stroke-width="1.5"
			stroke="currentColor"
			class="w-5 h-5"
		>
			<path
				stroke-linecap="round"
				stroke-linejoin="round"
				d="M6 12L3.269 3.126A59.768 59.768 0 0121.485 12 59.77 59.77 0 013.27 20.876L5.999 12zm0 0h7.5"
			/>
		</svg>
	</button>
</div>
