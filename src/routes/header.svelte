<script lang="ts">
	import Toggle from './toggle.svelte'
</script>

<nav class="navbar">
	<div class="navbar-start"></div>
	<div class="navbar-center"></div>
	<div class="navbar-end">
		<ul class="flex flex-row space-x-2 text-xl">
			<li>
				<a class="hover:bg-accent p-2" href="/">Home</a>
			</li>
			<li>
				<a class="hover:bg-accent p-2" href="/blog">Blog</a>
			</li>
			<li>
				<a class="hover:bg-accent p-2" href="https://github.com/jahandarm" target="_blank">Github</a
				>
			</li>
			<li>
				<Toggle />
			</li>
		</ul>
	</div>
</nav>
