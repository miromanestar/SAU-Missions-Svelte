<script>
	import Sidebar from './components/Sidebar.svelte'
	import ExploreSwiper from './components/ExploreSwiper.svelte'
</script>

<main>
	<Sidebar />
	<ExploreSwiper />
</main>

<style>
	main {
		display: grid;
		grid-template-columns: 12%;
		width: 100%;
		height: 100%;
		position: fixed;
	}
</style>