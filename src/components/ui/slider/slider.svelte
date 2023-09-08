<script lang="ts">
	import { Slider as SliderPrimitive } from "bits-ui";
	import { cn } from "$lib/util/tailwind-util";

	type $$Props = SliderPrimitive.Props;

	let className: $$Props["class"] = undefined;
	export let value: $$Props["value"] = [0];
	export { className as class };
</script>

<SliderPrimitive.Root
	bind:value
	class={cn("relative flex w-full touch-none select-none items-center", className)}
	{...$$restProps}
>
	<span class="relative h-1.5 w-full grow overflow-hidden rounded-full bg-primary/20">
		<SliderPrimitive.Range class="absolute h-full bg-primary" />
	</span>
	<SliderPrimitive.Thumb
		class="block w-4 h-4 border rounded-full shadow border-primary/50 bg-background transition-colors focus-visible:outline-none focus-visible:ring-1 focus-visible:ring-ring disabled:pointer-events-none disabled:opacity-50"
	/>
</SliderPrimitive.Root>
