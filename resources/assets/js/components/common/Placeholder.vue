<template>
	<component
		:is="$props.tag"
		class="x-placeholder relative w-full"
		:class="$props.ratio ? $props.ratio : 'pt-9/16'"
	>
		<transition name="x-fade">
			<slot />
		</transition>
	</component>
</template>

<script>
	export default {
		props: {
			tag: {
				type: String,
				default: 'div',
			},

			ratio: {
				type: String,
				default: null,
			},
		},
	}
</script>
