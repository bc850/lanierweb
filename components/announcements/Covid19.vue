<template>
  <div class="covid-19">
    <div class="covid-header abstract">
      <h2>COVID-19 Resource Center</h2>
    </div>
    <div class="covid-information abstract">
      <p>Access the latest tools and resources during the COVID-19 pandemic, at your fingertips.</p>
    </div>
    <div class="covid-button abstract">
      <button>Learn More</button>
    </div>
  </div>
</template>

<style lang="scss" scoped>
  .covid-19 {
    background-color: #0077c0;
    color: #fff;
    display: grid;
    grid-template-areas:
      "covid-header"
      "covid-information"
      "covid-button";
    grid-template-rows: 1fr 1fr 1fr;

    .abstract {
      display: flex;
      align-content: center;
      justify-content: center;
      height: 5rem;
    }

    .covid-header {
      grid-area: covid-header;

      h2 {
        font-size: 2.5rem;
        font-weight: 400;
        align-self: center;
      }
    }

    .covid-information {
      grid-area: covid-information;

      p {
        font-size: 1.5rem;
      }
    }

    .covid-button {
      grid-area: covid-button;

      button {
        border: 2px solid #fff;
        background-color: rgba(0, 119, 192, 0.6);
        color: #fff;
        font-size: 1.5rem;
        margin: 1rem;
        padding: 0.5rem;

        &:hover {
          background-color: #fff;
          color: rgba(0, 119, 192, 1);
        }
      }
    }
  }
</style>
