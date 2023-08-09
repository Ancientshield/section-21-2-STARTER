<template>
	<div id="app">
		<div class="scrollPosition">{{ offset }}</div>
	</div>
</template>

<script>
	import mixin from './mixin.js';

	export default {
		name: 'App',
		mixins: [mixin],
		data() {
			return {
				offset: 0,
			};
		},
		mounted() {
			console.log('App mounted lifecycle function');
		},
	};
</script>

<style>
	#app {
		width: 100%;
		height: 50000px;
		position: absolute;
	}

	.scrollPosition {
		position: fixed;
		overflow-y: scroll;
		left: 10px;
		right: 10px;
	}
</style>
