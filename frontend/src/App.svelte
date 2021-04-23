<script lang="ts">
	import Navbar from "./Navbar.svelte";
	import Home from "./Home.svelte";
	import { Router, Route, Link } from "svelte-routing";
</script>

<Router>
	<Navbar />
	<Route path="/">
		<Home />
	</Route>
</Router>

<style>
	:global(body) {
		margin: 0;
		padding: 0;
		text-align: center;
	}
</style>