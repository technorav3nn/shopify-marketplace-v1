<script lang="ts">
	import { Accordion as AccordionPrimitive } from "bits-ui";
	import { cn } from "$lib/util/tailwind-util";
	import { slide } from "svelte/transition";

	type $$Props = AccordionPrimitive.ContentProps;

	let className: $$Props["class"] = undefined;
	export let transition: $$Props["transition"] = slide;
	export let transitionConfig: $$Props["transitionConfig"] = {
		duration: 200,
	};

	export { className as class };
</script>

<AccordionPrimitive.Content
	class={cn("overflow-hidden text-sm", className)}
	{transition}
	{transitionConfig}
	{...$$restProps}
>
	<div class="pt-0 pb-4">
		<slot />
	</div>
</AccordionPrimitive.Content>
