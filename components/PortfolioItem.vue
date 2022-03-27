<template>
  <b-col lg="4" sm="6" class="mb-4">
    <div v-b-modal="modalId" class="portfolio-item">
      <a class="portfolio-link">
        <div class="portfolio-hover">
          <div class="portfolio-hover-content">
            <b-icon icon="search" scale="4" variant="dark" />
          </div>
        </div>
        <img class="img-fluid" :src="imageSrc" :alt="heading" />
      </a>
      <div class="portfolio-caption">
        <div class="portfolio-caption-heading">{{ heading }}</div>
        <div class="portfolio-caption-subheading text-muted">
          {{ subheading }}
        </div>
      </div>
    </div>
    <b-modal :id="modalId" size="lg" centered :title="heading" hide-footer>
      <b-carousel
        :id="modalId"
        v-model="currentSlide"
        :interval="4000"
        controls
        indicators
        background="#000"
        img-width="620"
        img-height="480"
        style="text-shadow: 1px 1px 2px #333"
      >
        <b-carousel-slide
          v-for="slide in slides"
          :key="slide.img"
          :img-src="slide.img"
        />
      </b-carousel>
    </b-modal>
  </b-col>
</template>

<script>
export default {
  props: {
    imageSrc: {
      type: String,
      required: true,
    },
    heading: {
      type: String,
      required: true,
    },
    subheading: {
      type: String,
      required: true,
    },
    slides: {
      type: Array,
      required: true,
    }
  },
  data() {
    return {
      showOverlay: false,
      modalId: `portfolioItemModal${this._uid}`,
      currentSlide: 0
    }
  }
}
</script>

<style scoped lang="scss">
.portfolio-item {
  .portfolio-link {
    position: relative;
    display: block;
    margin: 0 auto;

    border: 1px solid #877765;

    .portfolio-hover {
      display: flex;
      position: absolute;
      width: 100%;
      height: 100%;
      background: #877765;
      align-items: center;
      justify-content: center;
      opacity: 0;
      transition: opacity ease-in-out 0.25s;
    }

    &:hover .portfolio-hover {
      opacity: 1;
    }
  }
}
</style>
