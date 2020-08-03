<template>
  <div class="featured">
    <h2 class="title">Featured Products</h2>
    <div class="featured-products">
      <div class="products">
        <div class="product" v-for="fp in featured_products" :key="fp.id">
          <div class="bg-image" :style="{ 'background-image': 'url(' + fp.image + ')' }"></div>
          <div class="content">
            <p>{{fp.name}}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
   props: ['featured_products']
  }
</script>

<style lang="scss" scoped>
  .featured {
      display: grid;
      grid-template-areas:
        "left title right"
        "left featured right";
      grid-template-columns: "1fr 72rem 1fr";
      margin-bottom: 2rem;

    h2 {
      grid-area: title;
      font-weight: 300;
      font-size: 2.1rem;
    }

    .featured-products {
      grid-area: featured;

      .products {
        display: grid;
        grid-template-columns: repeat(4, 1fr);
        grid-template-rows: repeat(auto-fill);
        grid-row-gap: 1.5em;
        grid-column-gap: 1em;

        .product {
          width: 16rem;

          .bg-image {
            background-size: cover;
            min-height: 17rem;
            background-position: center;
          }

          .content {
            padding: 1rem;
            text-align: center;
          }
        }
      }
    }
  }
</style>
