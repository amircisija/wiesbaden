<template>
  <header class="fixed-top" id="header__wrapper">
    <div class="top__information--block py-3">
      <b-container class="top__information--wrapper">
        <b-row>
          <b-col>
            <p class="my-auto">Rufen Sie uns an: +123 456 789</p>
          </b-col>
          <b-col cols="3" class="ml-auto text-right">
            <a href="#">FB</a>
          </b-col>
        </b-row>
      </b-container>
    </div>
    <b-navbar toggleable="lg" type="dark" class="navbar is-transparent">
      <div class="container">
        <b-navbar-brand href="#">
          <!--           <b-img src="../static/img/logo.png" width="140px"></b-img> -->
        </b-navbar-brand>

        <b-navbar-toggle target="nav_collapse"/>

        <b-collapse is-nav id="nav_collapse">
          <b-navbar-nav class="ml-auto">
            <b-nav-item-dropdown offset="25" text="Home" left>
              <b-dropdown-item v-for="link in first_items" :key="link.id" href="#">{{ link.text }}</b-dropdown-item>
            </b-nav-item-dropdown>

            <b-nav-item-dropdown offset="25" text="Diagnostik" left>
              <b-dropdown-item v-for="link in second_items" :key="link.id" href="#">{{ link.text }}</b-dropdown-item>
            </b-nav-item-dropdown>

            <b-nav-item-dropdown offset="25" text="Medizinische Behandlungen" left>
              <b-dropdown-item v-for="link in third_items" :key="link.id" href="#">{{ link.text }}</b-dropdown-item>
            </b-nav-item-dropdown>

            <b-nav-item-dropdown offset="25" text="Ästhetik" left>
              <b-dropdown-item v-for="link in fourth_items" :key="link.id" href="#">{{ link.text }}</b-dropdown-item>
            </b-nav-item-dropdown>
            <b-nav-item-dropdown offset="25" text="Psychotherapie" left>
              <b-dropdown-item v-for="link in fifth_items" :key="link.id" href="#">{{ link.text }}</b-dropdown-item>
            </b-nav-item-dropdown>

            <b-nav-item-dropdown offset="25" text="Schulungen" left>
              <b-dropdown-item v-for="link in sixth_items" :key="link.id" href="#">{{ link.text }}</b-dropdown-item>
            </b-nav-item-dropdown>
          </b-navbar-nav>

          <!-- Right aligned nav items -->
          <b-navbar-nav class="ml-auto d-none">
            <b-nav-form>
              <b-form-input size="sm" class="mr-sm-2" type="text" placeholder="Search"/>
              <b-button size="sm" class="my-2 my-sm-0" type="submit">Search</b-button>
            </b-nav-form>

            <b-nav-item-dropdown text="Lang" right>
              <b-dropdown-item href="#">EN</b-dropdown-item>
              <b-dropdown-item href="#">ES</b-dropdown-item>
              <b-dropdown-item href="#">RU</b-dropdown-item>
              <b-dropdown-item href="#">FA</b-dropdown-item>
            </b-nav-item-dropdown>

            <b-nav-item-dropdown right>
              <!-- Using button-content slot -->
              <template slot="button-content">
                <em>User</em>
              </template>
              <b-dropdown-item href="#">Profile</b-dropdown-item>
              <b-dropdown-item href="#">Signout</b-dropdown-item>
            </b-nav-item-dropdown>
          </b-navbar-nav>
        </b-collapse>
      </div>
    </b-navbar>
  </header>
</template>
<script>
export default {
  data() {
    return {
      first_items: [
        { id: 1, text: "Über mich" },
        { id: 2, text: "Praxisräume" },
        { id: 3, text: "Kooperationen" },
        { id: 4, text: "Standorte" },
        { id: 5, text: "Warum Heilpraktiker ?!" },
        { id: 6, text: "Spezialisierungen" }
      ],
      second_items: [
        { id: 1, text: "Medizinische Anamnese" },
        { id: 2, text: "Körperuntersuchung" },
        { id: 3, text: "Bluttest" },
        { id: 4, text: "Stuhl / Urintest" }
      ],
      third_items: [
        { id: 1, text: "Infusionstherapie" },
        { id: 2, text: "Schmerztherapie" },
        { id: 3, text: "Ernährungstherapie" },
        { id: 4, text: "Aderlass" }
      ],
      fourth_items: [
        { id: 1, text: "Hyaluronbehandlung" },
        { id: 2, text: "Sculptra" }
      ],
      fifth_items: [
        { id: 1, text: "Gesprächstherapie" },
        { id: 2, text: "Verhaltenstherapie" },
        { id: 3, text: "Traumatherapie (EMDR)" }
      ],
      sixth_items: [
        { id: 1, text: "Einzeluntericht" },
        { id: 2, text: "Prüfungsvorbereitung" },
        { id: 3, text: "Intensiv learning" }
      ]
    };
  },
  mounted() {
    this.$nextTick(function() {
      window.addEventListener("scroll", function() {
        var header = document.getElementById("header__wrapper");
        var nav_classes = header.classList;
        if (document.documentElement.scrollTop >= 150) {
          if (nav_classes.contains("shrink") === false) {
            nav_classes.toggle("shrink");
          }
        } else {
          if (nav_classes.contains("shrink") === true) {
            nav_classes.toggle("shrink");
          }
        }
      });
    });
  }
};
</script>
<style lang="scss">
.top__information--wrapper {
  p {
    color: #fff;
  }
}

.navbar-dark .navbar-nav .nav-link {
  color: rgba(255, 255, 255, 0.59);
  padding: 5px 20px;
  transition: all 0.2s ease-in-out;
  font-size: 14px;
  &:hover {
    color: rgba(255, 255, 255, 0.89);
  }
}
.top__information--block {
  background: rgba(107, 105, 103, 0.4);
  transition: all 0.2s ease-in-out;
}
nav {
  padding: 1rem;
  transition: all 0.5s;
  background: rgba(66, 66, 66, 0.068);
}
.shrink {
  nav {
    padding: 0.3rem;
    /*     background: rgba(230, 208, 194, 0.92); */
    background: red;
    border-bottom: rgba(221, 221, 221, 0.28) 1px solid;
  }
  .top__information--block {
    background: rgba(143, 124, 117, 0.92);
  }
  .navbar-dark .navbar-nav .nav-link {
    color: rgba(143, 124, 117, 0.99);
    padding: 5px 20px;
    transition: all 0.2s ease-in-out;
    font-size: 14px;
  }
}
</style>