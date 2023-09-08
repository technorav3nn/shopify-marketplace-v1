<script lang="ts">
	import Button from "$components/ui/button/button.svelte";
	import { Moon, ShoppingBasketIcon, ShoppingCartIcon, Store, Sun, Sword } from "lucide-svelte";

	import { colorSchemeStore } from "$stores/color-scheme";
	import { Popover, PopoverContent, PopoverTrigger } from "$components/ui/popover";

	function toggleTheme() {
		console.log($colorSchemeStore);
		colorSchemeStore.set($colorSchemeStore === "dark" ? "light" : "dark");
	}
</script>

<header class="supports-backdrop-blur:bg-background/60 sticky top-0 z-40 w-full backdrop-blur">
	<div class="container mb-16 flex items-center justify-between pt-10 md:px-4">
		<section class="flex flex-row items-center">
			<p class="flex items-center gap-3 font-semibold">
				<Store size={20} class="inline-block" />Sitecrafing Solutions
			</p>
		</section>

		<section class="flex flex-row items-center gap-2">
			<div class="mr-5 flex items-center gap-5 text-sm">
				<a href="/home" class="text-foreground/60 transition-colors hover:text-foreground/80"
					>Home</a
				>
				<a href="/store" class="text-foreground/60 transition-colors hover:text-foreground/80"
					>Store</a
				>
				<a href="/about" class="text-foreground/60 transition-colors hover:text-foreground/80"
					>About</a
				>
			</div>
			<Button variant="ghost" size="icon" on:click={toggleTheme}>
				<Sun size={18} class="hidden dark:block" />
				<Moon size={18} class="block dark:hidden" />
			</Button>
			<Popover>
				<PopoverTrigger>
					<Button variant="ghost" size="icon">
						<ShoppingCartIcon size={18} />
					</Button>
				</PopoverTrigger>
				<PopoverContent class="w-40">
					<div class="grid gap-4">
						<div class="space-y-2">
							<h4 class="font-medium leading-none">Cart</h4>
						</div>
						<div class="flex items-center">
							<!-- Empty -->
							<div class="flex flex-col items-center justify-center space-y-2">
								<p class="text-sm text-gray-400">Your cart is empty</p>
							</div>
						</div>
					</div>
				</PopoverContent>
			</Popover>
		</section>
	</div>
</header>
