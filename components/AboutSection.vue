<template>
  <section class="page__section about__section" id="about__section--wrapper">
    <b-container>
      <b-row>
        <b-col xs="12" sm="8" md="7">
          <span>Willkommen bei</span>
          <h2 class="is__main--title--2">Heilpraktiker Wiesbaden</h2>
          <hr class="mb-5 mt-3">
          <p>Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit. Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut aliquip ex ea commodo consequat.</p>
          <p>Duis autem vel eum iriure dolor in hendrerit in vulputate velit esse molestie consequat, vel illum dolore eu feugiat nulla facilisis at vero eros et accumsan et iusto odio dignissim qui blandit praesent luptatum zzril delenit augue duis dolore te feugait nulla facilisi.</p>
          <p>Duis autem vel eum iriure dolor in hendrerit in vulputate velit esse molestie consequat, vel illum dolore eu feugiat nulla facilisis.</p>

          <b-button
            variant="primary"
            class="is__primary--1 has__color--1 is__primary__font mt-4"
          >Mehr erfahren</b-button>
        </b-col>
        <b-col xs="12" sm="4" md="5" class="p-5">
          <b-img src="~/static/img/img__1.jpg" class="elevation-4" fluid alt="Fluid image"/>
        </b-col>
      </b-row>
    </b-container>
  </section>
</template>
<style lang="scss">
.about__section {
  background: url("../static/img/bg__image--1.jpg");
}
.is__main--title--2 {
  color: #b5886d;
  font-size: 2.6em;
}
p {
  color: #4a4a4a;
}
</style>
