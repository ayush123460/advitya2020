<template>
    <div class="events">
        <Heading>
            <span>TECHNICAL</span>
            <span>EVENTS</span>
        </Heading>

        <section class="list">
            <div class="panel">
                Drone Workshop
            </div>
            <div class="panel">
                CubeVIT 2020
            </div>
            <div class="panel">
                Robo Race
            </div>
            <div class="panel">
                Line Follower
            </div>
            <div class="panel">
                FAD
            </div>
            <div class="panel">
                Coding Relay
            </div>
            <div class="panel">
                Science fair
            </div>
            <div class="panel">
                Workshop plus competition
            </div>
            <div class="panel">
                Poster Making
            </div>
        </section>
    </div>
</template>

<script>
import Heading from '@/components/Heading.vue';
export default {
    components: {
	  Heading
  },
  created() {
      window.addEventListener('scroll', this.handleScroll);
  },
  mounted() {
      return window.scrollTo({
          top: 0,
          behavior: 'smooth'
      });
  },
  destroyed() {
	  window.removeEventListener('scroll', this.handleScroll);
  },
  methods: {
	  handleScroll: function() {
		  if(window.scrollY > 60) {
			  document.querySelector('header').classList.add('homeScroll');
		  } else {
			  if(document.querySelector('header').classList.contains('homeScroll'))
			  	document.querySelector('header').classList.remove('homeScroll');
		  }
      }
  }
}
</script>