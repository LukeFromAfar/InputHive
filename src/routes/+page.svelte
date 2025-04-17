<script>
	import { Section, HeroHeader } from 'flowbite-svelte-blocks';
	import { Button } from 'flowbite-svelte';
    import { ChevronRight } from '@lucide/svelte';
</script>

<Section name="heroVisual" class="mt-[15dvh]">
	<div class="mr-auto place-self-center lg:col-span-7">
		<HeroHeader
			h1Class="max-w-2xl mb-4 text-4xl font-extrabold tracking-tight leading-none md:text-5xl xl:text-6xl dark:text-white"
			pClass="text-left max-w-2xl mb-6 font-light text-gray-500 lg:mb-8 md:text-lg lg:text-xl dark:text-gray-400 sm:px-0 lg:px-0 xl:px-0"
		>
			{#snippet h1()}InputHive - letting the users speak out.{/snippet}
			{#snippet paragraph()}From small indie studios to 10x developers, we are here to simplify the process of collecting and understanding user feedback. We make it easy to really make the change to a more user-focused workflow.{/snippet}
			<a href="/auth/login"><Button size="xl" color="red" class="mr-3 inline-flex items-center justify-center">Get started<ChevronRight class="-mr-1 ml-2 w-4" /></Button> </a>
			<a href="/"><Button color="light" size="xl" class="inline-flex items-center justify-center">See pricing</Button> </a>
		</HeroHeader>
	</div>

</Section>