<script>
	import Badge from "$components/ui/badge/badge.svelte";
	import { Button } from "$components/ui/button";
	import { ArrowRight } from "radix-icons-svelte";
</script>

<!-- Hero with tailwind css -->
<div class="flex items-center justify-center pt-10">
	<section>
		<Badge variant="outline" class="mb-6">New</Badge>

		<h1 class="text-6xl font-bold">Sitecrafing Solutions</h1>
		<p class="text-2xl font-semibold">The best place to buy and sell your items.</p>

		<Button variant="default" class="mt-6"
			>Get Started <ArrowRight size={18} class="ml-2 stroke-[10]" /></Button
		>
	</section>
</div>
