<template>
  <div id="app">
	  <HeaderComponent></HeaderComponent>
	  <router-view></router-view>
	  <FooterComponent></FooterComponent>
  </div>
</template>

<script>
import HeaderComponent from '@/components/HeaderComponent.vue';
import FooterComponent from '@/components/FooterComponent.vue';

export default {
	components: {
		HeaderComponent,
		FooterComponent
	}
}
</script>

<style lang="scss">
@import '@/scss/main.scss';
</style>
