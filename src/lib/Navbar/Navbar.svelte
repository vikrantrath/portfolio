<script lang="ts">
	import './navbar.scss';

	const navItems = [
		{
			label: 'About',
			url: '/about'
		},
		{
			label: 'Projects',
			url: '/projects'
		},
		{
			label: 'Experience',
			url: '/experience'
		}
	];
</script>

<div class="nav pt-4">
	<ul>
		{#each navItems as navItem (navItem.label)}
			<li><a class="nav-link" href={navItem.url}>{navItem.label}</a></li>
		{/each}
	</ul>
</div>

<style lang="scss">
	.nav-link:hover {
		color: rgba(94, 234, 212);
	}
</style>
