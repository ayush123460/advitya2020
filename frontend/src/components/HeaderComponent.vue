<template>
	<header>
		<div class="container">
			<div class="brand">
				<a href="/"><img src="@/assets/logo.png" alt="Advitya 2020 Logo"></a>
			</div>
			<nav>
				<a href="#events" @click="scroll($event)">Events</a>
				<a href="http://cyquest.in" target="_blank">Cyquest</a>
				<a href="https://www.thegameconquest.com" target="_blank">Gameconquest</a>
			</nav>
		</div>
	</header>
</template>

<script>
export default {
	methods: {
		scroll: function(event) {
			event.preventDefault();

			let el = document.querySelector('#events').offsetTop;

			return window.scrollTo({
				top: el,
				behavior: 'smooth'
			});
		}
	}
}
</script>
