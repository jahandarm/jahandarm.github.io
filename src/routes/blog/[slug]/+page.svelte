<script lang="ts">
	import { formatDate } from '$lib/utils';

	let { data } = $props();
</script>

<svelte:head>
	<title>{data.meta.title}</title>
	<meta property="og:type" content="article" />
	<meta property="og:title" content={data.meta.title} />
</svelte:head>

<article class="card space-y-2">
	<hgroup class="card-title flex flex-col justify-items-center space-y-2">
		<h1 class="text-2xl">{data.meta.title}</h1>
		<p class="text-sm">Published at {formatDate(data.meta.date)}</p>
		<div class="flex flex-row space-x-2">
			{#each data.meta.categories as category}
				<span class="surface-4 badge">&num;{category}</span>
			{/each}
		</div>
	</hgroup>

	<div class="card-body rounded-box shadow-md text-lg">
		<data.content />
	</div>
</article>
