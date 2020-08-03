<template>
  <div class="boxes">
    <div class="abstract demo">
      <h2>Need a Demo?</h2>
      <p>
        This is some text. It's some really good text
        and it is really just an example so that we can
        see what the spacing is going to look like.
      </p>
      <ArrowRight />
    </div>
    <div class="abstract quote">
      <h2>Get a Quote</h2>
      <p>
        This is some text. It's some really good text
        and it is really just an example so that we can
        see what the spacing is going to look like.
      </p>
      <ArrowRight />
    </div>
    <div class="abstract service">
      <h2>Service & Support</h2>
      <p>
        This is some text. It's some really good text
        and it is really just an example so that we can
        see what the spacing is going to look like.
      </p>
      <ArrowRight />
    </div>
    <div class="abstract locations">
      <h2>Locations</h2>
      <p>
        This is some text. It's some really good text
        and it is really just an example so that we can
        see what the spacing is going to look like.
      </p>
      <ArrowRight />
    </div>
  </div>
</template>

<script>
  import ArrowRight from '@/components/svgs/ArrowRight.vue'

  export default {
      components: {
        ArrowRight
      }
  }
</script>

<style lang="scss" scoped>
  .boxes {
    display: grid;
    grid-template-areas:
      "left demo quote service locations right";
    grid-template-columns: 1fr 18em 18rem 18rem 18rem 1fr;
    grid-column-gap: 1rem;
    height: 20rem;
    padding-bottom: 2rem;

    .abstract {
      color: #333;
      background-color: #f0f0f0;
      border-radius: 0.5rem;
      display: grid;
      grid-template-areas:
        "top"
        "middle"
        "bottom";
      grid-template-rows: "1fr 1fr 1fr";
      align-items: center;
      justify-items: center;
      padding: 0.5rem;

      &:hover {
        color: #fff;
        background-color: #333;

        svg {
          fill: #fff;
          stroke: #fff;
          stroke-width: 2;
        }
      }

      h2 {
        grid-area: top;
        font-weight: 200;
      }

      p {
        grid-area: middle;
        text-align: center;
        font-size: 1.2rem;
      }

      svg {
        grid-area: bottom;
        height: 2.5rem;
        width: auto;
      }
    }

    .demo {
      grid-area: demo;
    }

    .quote {
      grid-area: quote;
    }

    .service {
      grid-area: service;
    }

    .locations {
      grid-area: locations;
    }

  }
</style>
