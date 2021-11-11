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
		position: fixed;
		width: 100%;
		height: 100%;
		grid-template-columns: 12%;
	}
</style>