<template>
  <div class="lanier-video">
    <div class="video">
      <iframe height="540" width="100%" src="https://www.youtube.com/embed/ltYwYvsr1RM" frameborder="100" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    </div>
  </div>
</template>

<style lang="scss" scoped>
  .lanier-video {
    display: grid;
    grid-template-columns: 1fr 60rem 1fr;
    grid-template-areas: "left video right";
    padding: 2rem 0 2rem 0;

    .video {
      grid-area: video;
    }
  }
</style>
