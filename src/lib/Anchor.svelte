<script lang="ts">
	export let id: string;
</script>

<a class="anchor" {id} />

<style lang="scss">
	@import 'bootstrap/scss/mixins';
	@import 'bootstrap/scss/functions';
	@import 'bootstrap/scss/variables';

	a.anchor {
		display: block;
		position: relative;
		// Jumbotron padding = 4rem; NavBar height = 76px;
		top: calc(-4rem - 76px);
		visibility: hidden;
	}

	@include media-breakpoint-only(xs) {
		a.anchor {
			// Jumbotron padding = 2rem; NavBar height = 76px;
			top: calc(-2rem - 76px);
		}
	}
</style>
