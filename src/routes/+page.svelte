<script lang="ts">
	import Navbar from "$lib/components/Navbar.svelte";
	import Hero from "$lib/components/Hero.svelte";
	import FeatureOne from "$lib/components/FeatureOne.svelte";
	import FeatureTwo from "$lib/components/FeatureTwo.svelte";
	import FeatureGrid from "$lib/components/FeatureGrid.svelte";
	import TabFeature from "$lib/components/TabFeature.svelte";
	import StatsGrid from "$lib/components/StatsGrid.svelte";
	import BlogSection from "$lib/components/BlogSection.svelte";
	import CTASection from "$lib/components/CTASection.svelte";
	import Footer from "$lib/components/Footer.svelte";
</script>

<Navbar />
<main>
	<Hero />
	<FeatureOne />
	<FeatureTwo />
	<FeatureGrid />
	<TabFeature />
	<StatsGrid />
	<BlogSection />
	<CTASection />
</main>
<Footer />

