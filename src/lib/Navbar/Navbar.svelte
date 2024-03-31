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
			label: 'Contact & Social',
			url: '/contact'
		}
	];
</script>

<div class="nav">
	<ul>
		{#each navItems as navItem (navItem.label)}
			<li><a href={navItem.url}>{navItem.label}</a></li>
		{/each}
	</ul>
</div>
