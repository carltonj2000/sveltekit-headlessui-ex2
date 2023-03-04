<script lang="ts">
	import { Popover, PopoverButton, PopoverPanel } from '@rgossiaux/svelte-headlessui';
	export let name = 'name';
	export let label = 'label';
	export let heading = 'select a value';
	export let valueId = 0;
	export let valueDisplay = 'value';
	let popupName = `${name}-popup`;
</script>

<div class="mb-4 mt-1 max-w-xs">
	<input type="hidden" {name} value={valueId} />
	<label for={popupName}>{label} </label>
	<Popover id={popupName} class="relative">
		<PopoverButton
			class="relative w-full cursor-default rounded-md border border-gray-300 bg-white py-2 pl-3 pr-10 text-left shadow-sm focus:border-indigo-500 focus:outline-none focus:ring-1 focus:ring-indigo-500 sm:text-sm"
		>
			<span class="inlin-flex w-full truncate">{valueDisplay}</span>
			<span class="absolute inset-y-0 right-0 flex items-center pr-2 pointer-events-none">
				<svg
					xmlns="http://www.w3.org/2000/svg"
					fill="none"
					viewBox="0 0 24 24"
					stroke-width="1.5"
					stroke="currentColor"
					class="w-6 h-6 text-gray-400"
				>
					<path
						stroke-linecap="round"
						stroke-linejoin="round"
						d="M8.25 15L12 18.75 15.75 15m-7.5-6L12 5.25 15.75 9"
					/>
				</svg>
			</span>
		</PopoverButton>
		<PopoverPanel
			class="absolute z=10 bg-white px-5 py-4 border border-slate-300 mt-3 rounded-xl shadow-lg"
		>
			<h3 class="mb-3 text-lg font-semibold">{heading}</h3>
		</PopoverPanel>
	</Popover>
</div>
