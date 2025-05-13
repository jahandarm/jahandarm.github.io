<script>
	import { formatDate } from '$lib/utils';

	let { data } = $props();
</script>

<section>
	<ul class="list rounded-box shadow-md">
		<li class="p-4 pb-2 text-xs opacity-60 tracking-wide">My latest blog posts</li>

		{#each data.posts as post}
			<li class="list-row">
				<div class="list-col-grow">
					<a class="link text-lg" href="/blog/{post.slug}">{post.title}</a>
					<p class="list-col-wrap text-xs mt-2">{post.description}</p>
				</div>
				<p class="date">{formatDate(post.date)}</p>
			</li>
		{/each}
	</ul>
</section>
