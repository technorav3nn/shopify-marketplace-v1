<script>
	import Header from "$components/shell/Header.svelte";
	import "../app.postcss";
	import "@fontsource-variable/inter";
</script>

<div class="relative mx-auto flex min-h-screen max-w-[48rem] flex-col">
	<Header />
	<div class="px-[-12px]">
		<slot />
	</div>
</div>
