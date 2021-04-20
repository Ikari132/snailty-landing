<script lang="ts">
	import NavBar from '$lib/NavBar.svelte';
	import IntroSection from '$lib/IntroSection.svelte';
	import AboutSection from '$lib/AboutSection.svelte';
	import FeaturesSection from '$lib/FeaturesSection.svelte';
	import BrewingSection from '$lib/BrewingSection.svelte';
	import ClubSection from '$lib/ClubSection.svelte';
	import ArticlesSection from '$lib/ArticlesSection.svelte';
	import PricingSection from '$lib/PricingSection.svelte';
</script>

<main>
	<NavBar />

	<IntroSection />
	<AboutSection />
	<FeaturesSection />
	<BrewingSection />
	<ClubSection />
	<ArticlesSection />
	<PricingSection />
</main>

<style lang="scss">
	main {
		padding-top: 76px;
	}
</style>
