<template>
  <div class="jumbo">
    <div class="infobox">
      <div class="top infobox-item">
        <h2>Providing Water Infrastructure Solutions</h2>
      </div>
      <div class="middle infobox-item">
        <button>Infrastructure Rehabilitation</button>
        <button>Metering Solutions</button>
        <button>Waterworks</button>
      </div>
      <div class="bottom infobox-item">
        <h2>Since 1978.</h2>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
  .jumbo {
    background-image: url("https://lmsc.s3.amazonaws.com/lanierweb/DSC_4830.JPG");
    background-repeat: no-repeat;
    background-position: center center;
    background-size: cover;
    display: grid;
    grid-template-areas:
      "left mid right"
      "left mid right"
      "left mid right";
    grid-template-rows: 2rem 1fr 2rem;
    grid-template-columns: 2rem 1fr 2rem;
    align-items: center;
    justify-items: center;

    height: 100vh;

    .infobox {
      animation: 2s appear;
      grid-area: mid;
      color: #fff;
      height: 20rem;
      width: 100%;
      background-color: rgba(29, 29, 29, 0.6);
      border-radius: 0.5rem;
      display: grid;
      grid-template-areas:
        "top"
        "middle"
        "bottom";
      grid-template-rows: 1fr 1fr 1fr;

      .infobox-item {
        display: flex;
        align-self: center;
        justify-content: center;
      }

      .top {
        grid-area: top;
      }

      .middle {
        grid-area: middle;

        button {
          border: 2px solid white;
          color: #fff;
          background-color: rgba(29, 29, 29, 0.6);
          font-size: 1.5rem;
          width: 100%;
          margin: 1rem;
          padding: 0.5rem;

          &:hover {
            background-color: #fff;
            color: black;
          }
        }
      }

      .bottom {
        grid-area: bottom;
      }

      h2 {
        align-self: center;
        justify-self: center;
        font-size: 2.5rem;
        font-weight: 400;
      }
    }
  }

  @keyframes appear {
    0% {
      opacity: 0;
    }
  }
</style>
