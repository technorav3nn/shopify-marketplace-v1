<script lang="ts">
	import { cn } from "$lib/util/tailwind-util";
	import type { HTMLAttributes } from "svelte/elements";

	type $$Props = HTMLAttributes<HTMLTableSectionElement>;

	let className: $$Props["class"] = undefined;
	export { className as class };
</script>

<thead class={cn("[&_tr]:border-b", className)} {...$$restProps}>
	<slot />
</thead>
