<template>
  <div>
    <b-navbar toggleable="md" type="dark" variant="dark" sticky>
      <b-navbar-brand href="#">
        <img
          src="~/assets/images/logo.png"
          class="d-inline-block align-top"
          alt="logo"
        />
        J&S CONSTRUCTION
      </b-navbar-brand>

      <b-navbar-toggle target="nab-collapse"></b-navbar-toggle>

      <b-collapse id="nab-collapse" is-nav>
        <b-navbar-nav class="ml-auto">
          <b-nav-item href="#about-us">About us</b-nav-item>
          <b-nav-item href="#services">Services</b-nav-item>
          <b-nav-item href="#projects">Projects</b-nav-item>
          <b-button href="#contact" squared variant="outline-success"
            >CONTACT US</b-button
          >
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>

    <mast-header />

    <section id="about-us" class="page-section">
      <b-container>
        <b-row>
          <b-col class="text-center">
            <h2>About US</h2>
            <h3 class="section-subheading text-muted">
              Lorem ipsum dolor sit amet consectetur.
            </h3>
          </b-col>
        </b-row>
        <b-row>
          <b-col md="6">
            <p>
              Since 2013,<span class="font-weight-bold">J&S CONSTRUCTION</span>
              is dedicated to custom home building, renovating, and remodeling
              projects in the Chicago area.
            </p>
            <p>
              We can manage your project
              <span class="font-weight-bold"
                >from start to finish win a good schedule</span
              >
              , and you'll
              <span class="font-weight-bold">deal with one superintendent</span>
              regarding the day-to-day operations and communications.
            </p>
            <p>
              We'll work <span class="font-weight-bold">with you</span> to
              determine the parameters and specs of your project and bid
              accordingly.
            </p>
            <ul class="list-unstyled ml-4">
              <li><b-icon icon="check" variant="success" /> Vast Experience</li>
              <li>
                <b-icon icon="check" variant="success" /> Professional Team
              </li>
              <li><b-icon icon="check" variant="success" /> High Finish</li>
              <li>
                <b-icon icon="check" variant="success" /> Sustainable &
                Accountable
              </li>
            </ul>
            <div class="text-center mb-4">
              <b-button squared href="#projects">See some projects</b-button>
            </div>
          </b-col>
          <b-col md="6">
            <b-img
              src="~/assets/images/about-us.jpg"
              fluid
              alt="Truck"
              data-aos="truck-animation"
            />
          </b-col>
        </b-row>
      </b-container>
    </section>

    <section id="services" class="page-section bg-secondary">
      <b-container>
        <b-row>
          <b-col class="text-center">
            <h2>Our services</h2>
            <h3 class="section-subheading text-muted">
              Lorem ipsum dolor sit amet consectetur.
            </h3>
          </b-col>
        </b-row>
        <b-row>
          <service-item
            icon="card-checklist"
            heading="General Contractors"
            subheading="Lorem ipsum dolor sit amet consectetur"
            data-aos="fade-up"
          />
          <service-item
            icon="shop-window"
            heading="Interior & Exterior"
            subheading="Lorem ipsum dolor sit amet consectetur"
            data-aos="fade-up"
          />
          <service-item
            icon="house-door"
            heading="Remodeling & Renovations"
            subheading="Lorem ipsum dolor sit amet consectetur"
            data-aos="fade-up"
          />
          <service-item
            icon="plus"
            heading="Building Additions"
            subheading="Lorem ipsum dolor sit amet consectetur"
            data-aos="fade-up"
          />
        </b-row>
      </b-container>
    </section>

    <section id="projects" class="page-section">
      <b-container>
        <b-row>
          <b-col class="text-center">
            <h2>Projects</h2>
            <h3 class="section-subheading text-muted">
              Click on our projects to see some of our work
            </h3>
          </b-col>
        </b-row>
        <b-row>
          <portfolio-item
            v-for="(portfolioItem, id) in portfolioItems"
            :key="id"
            :image-src="portfolioItem.img"
            :heading="portfolioItem.heading"
            :subheading="portfolioItem.subheading"
            :slides="portfolioItem.carrouselSlides"
          />
        </b-row>
      </b-container>
    </section>

    <section id="contact" class="page-section bg-secondary">
      <b-container>
        <b-row>
          <b-col class="text-center">
            <h2>Contact us</h2>
            <h3 class="section-subheading text-muted">
              Call us or send us an email, we can help you to realize your nez project!
            </h3>
          </b-col>
        </b-row>
        <b-row class="text-center">
          <b-col>
            <b-button href="mailto:jbaptiste@gmail.com?subject=NewContact" variant="secondary" squared size="lg">
              <b-icon icon="envelope"></b-icon>
              jbaptiste@gmail.com
            </b-button>
          </b-col>
          <b-col>
            <b-button href="tel:060606006" variant="secondary" squared size="lg">
              <b-icon icon="telephone"></b-icon>
              060606006</b-button>
          </b-col>
        </b-row>
      </b-container>
    </section>

    <footer class="text-center p-4">
      <span>
        Copyright © General constructors {{ new Date().getFullYear() }}
      </span>
    </footer>

    <span class="instagram">
      <a href="https://instagram.com"><b-icon icon="instagram" variant="secondary"></b-icon></a>
    </span>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  data() {
    return {
      portfolioItems: [
        {
          heading: 'Pavilion in Hinsdale, IL',
          subheading: 'Lorem Ipsum',
          img: require('~/assets/images/portfolio/1/all.jpg'),
          carrouselSlides: [
            { img: require('~/assets/images/portfolio/1/all.jpg') },
            { img: require('~/assets/images/portfolio/1/floor.jpg') },
            { img: require('~/assets/images/portfolio/1/roof.jpg') },
          ],
        },
        {
          heading: "The Streamling's house",
          subheading: 'Lorem Ipsum',
          img: require('~/assets/images/portfolio/2/desk.jpg'),
          carrouselSlides: [
            { img: require('~/assets/images/portfolio/2/desk.jpg') },
            { img: require('~/assets/images/portfolio/2/fire-place.jpg') },
            { img: require('~/assets/images/portfolio/2/living-room.jpg') },
          ],
        },
        {
          heading: 'House in Olympia fields, IL',
          subheading: 'Lorem Ipsum',
          img: require('~/assets/images/portfolio/3/kitchen.jpg'),
          carrouselSlides: [
            { img: require('~/assets/images/portfolio/3/kitchen.jpg') },
            { img: require('~/assets/images/portfolio/3/room.jpg') },
            { img: require('~/assets/images/portfolio/3/stairs.jpg') },
            { img: require('~/assets/images/portfolio/3/tube.jpg') },
          ],
        },
      ],
    }
  },
}
</script>

<style lang="scss">
html {
  scroll-behavior: smooth;

  .navbar > .navbar-brand > img {
    height: 2rem;
  }

  .page-section {
    padding: 6rem 0;
    h2.section-heading,
    .section-heading.h2 {
      font-size: 2.5rem;
      margin-top: 0;
      margin-bottom: 1rem;
    }
    h3.section-subheading,
    .section-subheading.h3 {
      font-size: 1rem;
      font-weight: 400;
      font-style: italic;
      font-family: 'Roboto Slab', -apple-system, BlinkMacSystemFont, 'Segoe UI',
        Roboto, 'Helvetica Neue', Arial, sans-serif, 'Apple Color Emoji',
        'Segoe UI Emoji', 'Segoe UI Symbol', 'Noto Color Emoji';
      margin-bottom: 4rem;
    }
  }

  //TO improve
  .navbar {
    border-bottom: 1px solid #877765;
  }
  .bg-secondary {
    background-color: #877765;
    background-image: linear-gradient(135deg, #54a6ff 0%, #dcd7c0 100%);
  }
}

[data-aos="truck-animation"] {
  opacity: 0;
  transition-property: transform, opacity;

  &.aos-animate {
    opacity: 1;
  }

  @media screen and (min-width: 768px) {
    transform: translateX(100px);

    &.aos-animate {
      transform: translateX(0);
    }
  }
}

.instagram {
  background-color: #1d1d1d;
  position: fixed;
  top: 100px;
  font-size: 30px;
  padding: 5px 10px 2px 10px;
  border-radius: 0 8px 8px 0;
  border: 1px solid #877765;
  left: 0;
}
</style>
