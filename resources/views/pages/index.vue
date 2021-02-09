<template>
	<div class="x-container flex flex-col items-center justify-center min-h-screen h-full">
		<logo />

		<h1
			:class="[
				'text-center max-w-2xl x-h1 mt-2',
				'xl:max-w-3xl xl:mt-5',
			]"
			v-text="$data.model.title"
		/>

		<p
			:class="[
				'x-h5 max-w-sm text-center font-light',
				'mt-4 md:mt-6 xl:mt-8',
			]"
			v-text="$data.model.content"
		/>
	</div>
</template>

<script>
	import head from '../../assets/js/mixins/head';

	export default {
		mixins: [head],

		layout: 'simple',

		async asyncData ({ $content }) {
			return await $content('index').fetch();
		},
	};
</script>
