<template>
	<div class="home">
		<div class="overlay"></div>
		<section class="hero">
			<video autoplay muted loop>
				<source src="@/assets/bg.mp4" type="video/mp4">
			</video>
			<div class="hero__text">feel the enigma.</div>
			<div class="hero__scroll">
				<div class="line"></div>
				scroll
				<div class="line"></div>
			</div>
		</section>
		<section class="events" id="events">
			<Heading>
				<span>our</span>
				<span>events</span>
			</Heading>
			<div class="cards">
				<div class="card tech">
					<div class="header">technical</div>
					<div class="body">
						<i class="far fa-calendar-plus"></i> 26 March 2020
						<br>
						<br>
						<router-link to="/events">Know More</router-link>
					</div>
				</div>
				<div class="card cult">
					<div class="header">cultural</div>
					<div class="body">
						<i class="far fa-calendar-plus"></i> 27 &amp; 28 March 2020
						<br>
						<br>
						<router-link to="/events">Coming Soon</router-link>
					</div>
				</div>
				<div class="card sports">
					<div class="header">sports</div>
					<div class="body">
						<i class="far fa-calendar-plus"></i> 24 &amp; 25  March 2020
						<br>
						<br>
						<router-link class="inverse" to="/sports">Know More</router-link>
					</div>
				</div>
				<div class="card pro">
					<div class="header">pro show</div>
					<div class="body">
						<i class="far fa-calendar-plus"></i> 28 March 2020
						<br>
						<br>
						<router-link to="/events">Coming Soon</router-link>
					</div>
				</div>
			</div>
		</section>
	</div>	
</template>

<script>
import Heading from '@/components/Heading.vue';

export default {
  name: 'Home',
  components: {
	  Heading
  },
  created() {
	  window.addEventListener('scroll', this.handleScroll);
  },
  destroyed() {
	  window.removeEventListener('scroll', this.handleScroll);
  },
  methods: {
	  handleScroll: function() {
		  if(window.scrollY > 200) {
			  document.querySelector('header').classList.add('homeScroll');
		  } else {
			  if(document.querySelector('header').classList.contains('homeScroll'))
			  	document.querySelector('header').classList.remove('homeScroll');
		  }
	  }
  }
}
</script>
