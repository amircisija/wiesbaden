<template>
  <section class="color__1" id="service__list--wrapper">
    <b-container class="pb-5 pt-0">
      <b-row>
        <b-col v-for="item in items" :key="item.id">
          <div :class="`service__boxes service__boxes--${item.class}`">
            <div class="custom-border-gap bg-image">
              <span class="custom-border-gap__border left"></span>
              <span class="custom-border-gap__border right"></span>
              <div class="service_title">
                <h3>{{ item.title }}</h3>
              </div>
            </div>
          </div>
        </b-col>
      </b-row>
      <b-row>
        <b-col class="text-center mx-auto" cols="4">
          <b-button
            variant="primary"
            class="is__primary--1 has__color--1 is__primary__font"
          >Mehr erfahren</b-button>
        </b-col>
      </b-row>
    </b-container>
  </section>
</template>
<script>
export default {
  data() {
    return {
      items: [
        { id: 1, title: "körper", class: "1" },
        { id: 2, title: "gesicht", class: "2" },
        { id: 3, title: "injektion", class: "3" },
        { id: 4, title: "brüste", class: "4" }
      ]
    };
  }
};
</script>
<style scoped lang="scss">
.service__boxes {
  background: purple;
  min-height: 400px;
}
.service__boxes {
  background-position: center !important;
  background-size: cover !important;
  background-repeat: no-repeat;
  position: relative;
  background-position: center top;
  height: 492px;
  margin-bottom: 2rem;
}
.service__boxes--1 {
  background: url("../static/img/s__1.jpg");
  bottom: 50px;
}
.service__boxes--2 {
  background: url("../static/img/s__2.jpg");
  bottom: 80px;
}
.service__boxes--3 {
  background: url("../static/img/s__3.jpg");
  bottom: 50px;
}
.service__boxes--4 {
  background: url("../static/img/s__4.jpg");
  bottom: 80px;
}
.service__boxes:before {
  content: "";
  background: rgba(0, 0, 0, 0.3);
  position: absolute;
  left: 0px;
  top: 0px;
  width: 100%;
  height: 100%;
  z-index: 1;
}
.custom-border-gap.bg-image {
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  height: 100%;
}
.custom-border-gap__border {
  display: block;
  position: absolute;
  top: 0;
  left: 0;
  z-index: 1;
  width: 100%;
  height: 100%;
}
.custom-border-gap__border.left::before,
.custom-border-gap__border.left::after {
  top: 1rem;
  left: 1rem;
}

.custom-border-gap__border::before,
.custom-border-gap__border::after {
  position: absolute;
  content: "";
  background: #fff;
  z-index: 1;
  transition: width 0.4s ease, height 0.4s ease;
}
.custom-border-gap__border::before {
  width: 1px;
  height: 80%;
}
.right {
  float: right !important;
}
.left {
  float: left !important;
}
.custom-border-gap__border.right::before,
.custom-border-gap__border.right::after {
  bottom: 1rem;
  right: 1rem;
}
.custom-border-gap__border::before,
.custom-border-gap__border::after {
  position: absolute;
  content: "";
  background: #fff;
  z-index: 1;
  transition: width 0.4s ease, height 0.4s ease;
}
.custom-border-gap__border::before {
  width: 1px;
  height: 80%;
}
.custom-border-gap__border::after {
  height: 1px;
  width: 80%;
}
.service_title {
  text-align: center;
  z-index: 1;
  position: relative;
  padding-top: 370px;
}
.service_title h3 {
  text-align: center;
  text-transform: uppercase;
  color: #fff;
  font-size: 30px;
}
.service_title h3::before {
  content: "";
  width: 50px;
  height: 2px;
  background: #fff;
  display: block;
  position: relative;
  top: 40px;
  left: 0;
  margin: auto;
}
.service_title p {
  font-size: 16px;
  line-height: 28px;
  color: #fff;
  letter-spacing: 0.34px;
  margin-top: 20px;
  text-transform: uppercase;
}

.custom-border-gap:hover .custom-border-gap__border::before {
  height: calc(100% - 1rem * 2);
}
.custom-border-gap:hover .custom-border-gap__border::after {
  width: calc(100% - 1rem * 2);
}

body,
p,
h1,
h2,
h3,
h4,
h5,
h6 {
  margin: 0px;
  padding: 0px;
  font-family: "Poppins", sans-serif;
}
a.navbar-brand {
  width: 245px;
}
ul {
  list-style: none;
  margin: 0px;
  padding: 0px;
}
a {
  text-decoration: none;
  font-family: "Poppins", sans-serif;
}
a:hover,
a:focus {
  text-decoration: none;
  outline: none;
  font-family: "Poppins", sans-serif;
}
h1,
h2,
h3,
h4,
h5,
h6 {
  /*font-family: 'Roboto', sans-serif;*/
  font-family: "Poppins", sans-serif;
  color: #000;
}
p {
  font-size: 16px;
  color: #555;
  line-height: 26px;
  /*font-family: 'Open Sans', sans-serif;*/
  font-family: "Poppins", sans-serif;
}
</style>