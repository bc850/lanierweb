<template>
	<div class="header">
    <div class="nav-top">
      <span>1-800-342-1381</span>
      <span>|</span>
      <span>Contact Us</span>
    </div>
		<div class="nav-bottom">
      <LogoWhite />
      <p>Who We are</p>
      <p>What We Do</p>
      <p>Products</p>
      <p>Pipeline Knowledge Center</p>
    </div>
	</div>
</template>

<script>
	import LogoWhite from '@/components/logos/LogoWhite.vue'

	export default {
		components: {
			LogoWhite
		}
	}
</script>

<style lang="scss">
	.header {
		background: #C62127;
    color: #fff;
    display: grid;
    font-size: 1.1rem;
    grid-template-columns: 1fr 60rem 1fr;
    grid-template-areas:
      "left nav-top right"
      "left nav-bottom right";

    .nav-top {
      display: flex;
      align-items: center;
      grid-area: nav-top;
      justify-content: flex-end;
      height: 2.5rem;

      span {
        margin-right: 0.5rem;

        &:last-child {
          margin-right: 0;
        }
      }
    }

    .nav-bottom {
      display: flex;
      grid-area: nav-bottom;
      align-items: center;
      justify-content: space-between;

      .brand {
        height: 4.5rem;
        width: auto;
      }
    }
	}
</style>
