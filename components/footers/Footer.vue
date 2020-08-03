<template>
  <div class="footer">
    <div class="content">
      <LogoDark />
      <p>Copyright © 2020 Lanier Municipal Supply Co., Inc. | All Rights Reserved</p>
    </div>
  </div>
</template>

<script>
  import LogoDark from '@/components/logos/LogoDark'

  export default {
    components: {
      LogoDark
    }
  }
</script>

<style lang="scss" scoped>
  .footer {
    background-color: #222222;
    display: grid;
    grid-template-areas:
      "left content right";
    grid-template-columns: 2rem 1fr 2rem;
    height: 10rem;

    svg {
      height: 3.5rem;
      width: auto;
    }

    .content {
      color: #fff;
      grid-area: content;
      align-self: center;
      justify-self: flex-start;

      p {
        font-size: 0.9rem;
      }
    }
  }
</style>
