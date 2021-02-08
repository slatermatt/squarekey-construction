<template>
	<div
		v-cloak
		class="flex flex-col min-h-screen"
	>
		<main class="relative flex-auto z-site-content">
			<intersect @intersect="$data.hidden = true">
				<transition
					leave-active-class="transition-opacity duration-1000"
					leave-to-class="opacity-0"
				>
					<span
						v-if="!$data.hidden"
						class="absolute inset-0 w-full h-full bg-black"
					/>
				</transition>
			</intersect>

			<Nuxt />
		</main>
	</div>
</template>

<script>
	export default {
		data() {
			return {
				hidden: false,
			};
		},
	};
</script>
