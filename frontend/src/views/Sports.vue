<template>
    <div class="sports">
        <Heading>
            <span>SPORTS</span>
            <span>EVENTS</span>
        </Heading>
        <section class="download">
            <a href="sports_rules.pdf" target="_blank">Click here</a> to download the rules sheet.
            For further details contact: <br>
            Akash Vats &amp; Priyan Kapoor - 8397969428, 6398248185
        </section>
        <section class="posters">
            <img src="@/assets/POSTERS-01.png">
            <div class="gap"></div>
            <img src="@/assets/POSTERS-02.png">
            <div class="gap"></div>
            <img src="@/assets/POSTERS-03.png">
            <div class="gap"></div>
            <img src="@/assets/POSTERS-04.png">
            <div class="gap"></div>
            <img src="@/assets/POSTERS-05.png">
            <div class="gap"></div>
            <img src="@/assets/POSTERS-06.png">
            <div class="gap"></div>
            <img src="@/assets/POSTERS-07.png">
            <div class="gap"></div>
            <img src="@/assets/POSTERS-08.png">
            <div class="gap"></div>
            <img src="@/assets/POSTERS-09.png">
            <div class="gap"></div>
            <img src="@/assets/POSTERS-10.png">
            <div class="gap"></div>
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