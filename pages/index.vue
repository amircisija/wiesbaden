<template>
  <section id="carousel__wrapper">
    <section class="bgimage jarallax" data-jarallax data-speed="0.2">
      <div class="overlay__shadow"></div>
      <div class="container h-100">
        <div class="row h-100 align-items-center">
          <div class="col-lg-9 col-md-9 col-sm-12 col-xs-12">
            <h2 class="header__title">Schönheit und Zufriedenheit</h2>
            <p
              class="header__text mb-4"
            >Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore</p>
            <b-button
              variant="primary"
              class="is__primary--1 has__color--1 is__primary__font"
            >Mehr erfahren</b-button>
          </div>
        </div>
      </div>
    </section>
    <ServiceList/>
    <AboutSection/>
    <FeatureSection/>
    <CtaSection/>
    <ContactSection/>
  </section>
</template>

<script>
import Carousel from "~/components/Carousel.vue";
import ServiceList from "~/components/ServiceList.vue";
import AboutSection from "~/components/AboutSection.vue";
import FeatureSection from "~/components/FeatureSection.vue";
import CtaSection from "~/components/CtaSection.vue";
import ContactSection from "~/components/ContactSection.vue";
export default {
  components: {
    Carousel,
    ServiceList,
    AboutSection,
    FeatureSection,
    CtaSection,
    ContactSection
  }
};
</script>

<style lang="scss">
.bgimage {
  width: 100%;
  height: 100vh;
  background: url("../static/img/slide__1.jpg");
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
  background-attachment: fixed;
  position: relative;
  overflow: hidden;
  .main__title {
    color: #fff;
    font-family: "Poppins", sans-serif;
    font-size: 5.6em;
    font-weight: 500;
    letter-spacing: 1px;
  }
  span {
    color: #fff;
    font-size: 1.6em;
    text-transform: uppercase;
    letter-spacing: 2px;
    color: #fff;
  }
  p {
    color: #fff;
    font-size: 1.4em;
    font-weight: 300;
  }
  .header__title {
    font-size: 4em;
    color: #fff;
  }
  .header__text {
    color: #fff;
  }
}
p {
  font-family: "Poppins", sans-serif;
}
.color__1 {
  background: #3b414d;
}
.page__section {
  padding: 100px 0;
}
.is__primary--1 {
  padding: 10px 60px;
  border-radius: 0;
}
.has__color--1 {
  background: #867972;
  border: 1px solid #e6d0c2;
}
.is__primary__font {
  font-family: "Cormorant", serif;
}
.elevation-4 {
  transition: all 0.2s ease-in-out;
  box-shadow: 0px 2px 4px -1px rgba(0, 0, 0, 0.2),
    0px 4px 5px 0px rgba(0, 0, 0, 0.14), 0px 1px 10px 0px rgba(0, 0, 0, 0.12) !important;
  &:hover {
    box-shadow: 0px 6px 6px -3px rgba(0, 0, 0, 0.2),
      0px 10px 14px 1px rgba(0, 0, 0, 0.14),
      0px 4px 18px 3px rgba(0, 0, 0, 0.12) !important;
  }
}
.overlay__shadow {
  position: absolute;
  background: rgba(102, 59, 27, 0.32);
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
  right: 0;
}
</style>
