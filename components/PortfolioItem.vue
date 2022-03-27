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
        id="carousel-1"
        v-model="slide"
        :interval="4000"
        controls
        indicators
        background="#ababab"
        img-width="1024"
        img-height="480"
        style="text-shadow: 1px 1px 2px #333"
        @sliding-start="onSlideStart"
        @sliding-end="onSlideEnd"
      >
        <!-- Slides with custom text -->
        <b-carousel-slide
          caption="First slide"
          text="Nulla vitae elit libero, a pharetra augue mollis interdum."
          :img-src="require('~/assets/images/portfolio/1/roof.jpg')"
        >
          <h1>Hello world!</h1>
        </b-carousel-slide>
        <b-carousel-slide
          caption="First slide"
          text="Nulla vitae elit libero, a pharetra augue mollis interdum."
          :img-src="require('~/assets/images/portfolio/1/floor.jpg')"
        >
          <h1>Hello world!</h1>
        </b-carousel-slide>
        <b-carousel-slide
          caption="First slide"
          text="Nulla vitae elit libero, a pharetra augue mollis interdum."
          :img-src="require('~/assets/images/portfolio/1/all.jpg')"
        >
          <h1>Hello world!</h1>
        </b-carousel-slide>

        <!-- Slide with blank fluid image to maintain slide aspect ratio -->
        <b-carousel-slide caption="Blank Image" img-blank img-alt="Blank image">
          <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse
            eros felis, tincidunt a tincidunt eget, convallis vel est. Ut
            pellentesque ut lacus vel interdum.
          </p>
        </b-carousel-slide>
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
  },
  data() {
    return {
      showOverlay: false,
      modalId: `portfolioItemModal${this._uid}`,
      slide: 0,
      sliding: null,
    }
  },
  methods: {
    onSlideStart(slide) {
      this.sliding = true
    },
    onSlideEnd(slide) {
      this.sliding = false
    },
  },
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
