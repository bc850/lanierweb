<template>
	<div>
		<Navbar />
		<Nuxt />
    <Footer />
	</div>
</template>

<script>
  import Footer from '@/components/footers/Footer.vue'
  import Navbar from '@/components/headers/Navbar.vue'

	export default {
		components: {
      Footer,
      Navbar
		}
	}
</script>

<style lang="scss">
	body {
    font-family: 'Raleway', sans-serif;
		margin: 0;
		padding: 0;
	}
</style>
