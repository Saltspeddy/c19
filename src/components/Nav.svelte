<script>
	let isOpen=false;
	export let segment;
	function toggleNav(){
		isOpen = !isOpen;
	}
</script>

<style>

		
</style>

<nav class="navbar" aria-label="main navigation" >
	<div class = "navbar-brand">
		<a href="/" class="navbar-item" class:is-active={segment === undefined}>
			<img src="logo.jpg" alt="asta e">
		</a>
		<span
		class="navbar-burger"
		class:is-active={isOpen}
		on:click={toggleNav}
		aria-label="menu"
		aria-expanded="false"
		>
		<span aria-hidden="true"/>
		<span aria-hidden="true"/>
		<span aria-hidden="true"/>
		</span>
	</div>
	<div class="navbar-menu" class:is-active={!isOpen}>
		<div class="navbar-start"></div>
			<a href="/" class="navbar-item" class:is-active={segment === undefined}
			>Home</a>
			<a href="/about" class="navbar-item" class:is-active={segment === 'about'}>About</a>
	</div>
</nav>