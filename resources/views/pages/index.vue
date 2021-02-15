<template>
	<div class="x-container flex flex-col items-center justify-center min-h-screen h-full">
		<div class="max-w-5xl">
			<logo />

			<h1
				:class="[
					'x-h1 x-fade mt-2',
					'xl:mt-5',
				]"
				v-text="$data.model.title"
			/>

			<p
				:class="[
					'x-h5 max-w-md font-light',
					'mt-4 md:mt-6 xl:mt-8',
				]"
				v-text="$data.model.content"
			/>
		</div>
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
