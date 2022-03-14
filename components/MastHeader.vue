<template>
  <header class="masthead">
    <div class="container">
      <div class="masthead-subheading">J&S CONSTRUCTION</div>
      <div class="masthead-heading text-uppercase">Residential & Commercial</div>
      <b-button size="lg" squared variant="secondary" href="#services">Tell Me More</b-button>
    </div>
  </header>
</template>

<style lang="scss" scoped>
.masthead {
  padding-top: 10.5rem;
  padding-bottom: 6rem;
  text-align: center;
  color: #877765;
  text-shadow: 1px 1px 2px #1D1D1D, 0 0 25px #1D1D1D, 0 0 5px #1D1D1D;
  background-image: url('~/assets/images/header.jpg');
  background-repeat: no-repeat;
  background-attachment: scroll;
  background-position: center center;
  background-size: cover;

  .masthead-subheading {
    font-size: 1.5rem;
    font-style: italic;
    line-height: 1.5rem;
    margin-bottom: 25px;
  }
  .masthead-heading {
    font-size: 3.25rem;
    font-weight: 700;
    line-height: 3.25rem;
    margin-bottom: 2rem;
  }
}

@media (min-width: 768px) {
  .masthead {
    padding-top: 17rem;
    padding-bottom: 12.5rem;
    .masthead-subheading {
      font-size: 2.25rem;
      font-style: italic;
      line-height: 2.25rem;
      margin-bottom: 2rem;
    }
    .masthead-heading {
      font-size: 4.5rem;
      font-weight: 700;
      line-height: 4.5rem;
      margin-bottom: 4rem;
    }
  }
}
</style>
