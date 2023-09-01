<div class="flex flex-col items-center gap-4">
	<h1 class="text-4xl font-semibold">Chatbot UI</h1>

	<div class="border border-surface-400 rounded-md p-4 flex flex-col gap-2 w-full">
		<div class="flex flex-col gap-1">
			<label for="Model"> Model </label>
			<select class="select rounded-md" name="Model" id="Model">
				<option value="gpt-3.5-turbo">Default (GPT-3.5)</option>
				<option value="gpt-3.5-turbo">(GPT-3.5)</option>
			</select>
		</div>
		<a class="anchor flex text-sm no-underline" href="https://platform.openai.com/account/usage">
			<span
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
						d="M13.5 6H5.25A2.25 2.25 0 003 8.25v10.5A2.25 2.25 0 005.25 21h10.5A2.25 2.25 0 0018 18.75V10.5m-10.5 6L21 3m0 0h-5.25M21 3v5.25"
					/>
				</svg>
			</span>View Account Usage</a
		>
		<div class="flex flex-col gap-1">
			<label for="System Prompt"> System Prompt </label>
			<textarea
				class="w-full text-left rounded-lg border border-neutral-200 bg-transparent px-4 py-3 text-neutral-900 dark:border-neutral-600 dark:text-neutral-100"
				placeholder="Enter a prompt or type &quot;/&quot; to select a prompt..."
				style="resize: none; max-height: 300px; overflow: hidden; height: 64px; bottom: 64px;"
			/>
		</div>
		<div class="flex flex-col gap-1">
			<label for="Temperature" class="mb-2 text-left text-neutral-700 dark:text-neutral-400"
				>Temperature</label
			><span class="text-[12px] text-black/50 dark:text-white/50 text-sm"
				>Higher values like 0.8 will make the output more random, while lower values like 0.2 will
				make it more focused and deterministic.</span
			><span class="mt-2 mb-1 text-center text-neutral-900 dark:text-neutral-100">0.9</span><input
				class="cursor-pointer"
				type="range"
				min="0"
				max="1"
				step="0.1"
				value="0.9"
			/>
			<ul class="w mt-2 pb-8 flex justify-between px-[24px] text-neutral-900 dark:text-neutral-100">
				<li class="flex justify-center"><span class="absolute">Precise</span></li>
				<li class="flex justify-center"><span class="absolute">Neutral</span></li>
				<li class="flex justify-center"><span class="absolute">Creative</span></li>
			</ul>
		</div>
	</div>
</div>
