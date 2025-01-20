<script lang="ts">
	import BrunoWidget from "./BrunoWidget.svelte";
	import FabiaWidget from "./FabiaWidget.svelte";

	interface Props {
		version: "students" | "dogpatch";
	}

	const { version }: Props = $props();

	const randomBoolean = () => Math.random() >= 0.5;
</script>

<h1 class="mb-6 text-6xl font-bold">Help Us</h1>

<p>
	We're Fabia and Bruno. We met during the <a href="https://joinfounders.co/">Founders programme</a>
	at <a href="https://dogpatchlabs.com/">Dogpatch Labs</a> with a common interest in learning how
	people
	{#if version === "dogpatch"}
		generate & share knowledge.
	{:else if version === "students"}
		generate, share, and research knowledge.
	{/if}
</p>

<h2 class="my-4 mt-6 text-4xl font-semibold">Why we put up these posters</h2>
<p>
	We want to learn how you do, keep track of, and share knowledge work. If something doesn't work
	well for you, we'd love to hear about it. Google Docs being a pain? Feel free to vent.
</p>

<h2 class="my-4 mt-6 text-4xl font-semibold">What we're asking for</h2>
<p>
	We're looking for 15 minutes of your time to get to know you, understand your way of thinking, and
	how you approach projects. 5 random people who contact us will get a €20 Amazon voucher as a thank
	you.
</p>

<h2 class="my-4 mt-6 text-4xl font-semibold">What this isn't</h2>
<p>
	This isn't a sales pitch. This isn't a SaaS landing page. We geniunely just want to learn about
	you and your experiences.
</p>

<h2 class="my-4 mt-6 text-4xl font-semibold">Let's do it</h2>
{#if randomBoolean()}
	<BrunoWidget />
{:else}
	<FabiaWidget />
{/if}
