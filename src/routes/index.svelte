<script lang="ts">
	import NavBar from '$lib/NavBar.svelte';
	import IntroSection from '$lib/IntroSection.svelte';
	import AboutSection from '$lib/AboutSection.svelte';
</script>

<main>
	<NavBar />

	<IntroSection />
	<AboutSection />
</main>

<style lang="scss">
	main {
		padding-top: 76px;
	}
</style>
