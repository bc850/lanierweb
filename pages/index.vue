<template>
  <div class="lanier">
    <Jumbo />
    <Covid-19 />
    <Video />
    <Boxes />
    <FeaturedProducts :featured_products="featured_products" />
  </div>
</template>

<script>
  import axios from 'axios'
  import Boxes from '@/components/home/Boxes.vue'
  import Covid19 from '@/components/announcements/Covid19.vue'
  import FeaturedPRoducts from '@/components/home/FeaturedProducts.vue'
  import Jumbo from '@/components/home/Jumbo.vue'
  import Video from '@/components/home/Video.vue'

  export default {
    components: {
      Boxes,
      Covid19,
      FeaturedPRoducts,
      Jumbo,
      Video
    },

    data() {
      return {
        featured_products: []
      }
    },

    asyncData({$axios}) {
      return $axios.get("/featured-products")
      .then(res => {
        return {featured_products: res.data}
      })
    },
  }
</script>

<style lang="scss" scoped>

</style>
