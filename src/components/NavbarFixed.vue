<template>
  <div class="fixed-top">
    <b-navbar toggleable="lg" type="dark">
      <b-navbar-brand to="/#homeSection">
        <img src="../assets/logo3.svg" alt="logo" />
      </b-navbar-brand>

      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav>
          <b-nav-item to="/#homeSection">
            {{ data[langId].elements[0].el1 }}
          </b-nav-item>
          <b-nav-item to="/#aboutSection">
            {{ data[langId].elements[0].el2 }}
          </b-nav-item>
          <b-nav-item to="/#skillsSection">
            {{ data[langId].elements[0].el3 }}
          </b-nav-item>
          <b-nav-item to="/#ProjectsSection">
            {{ data[langId].elements[0].el4 }}
          </b-nav-item>
          <b-nav-item to="/#contactSection">
            {{ data[langId].elements[0].el5 }}
          </b-nav-item>
        </b-navbar-nav>

        <!-- Right aligned nav items -->
        <b-navbar-nav class="ml-auto">
          <b-nav-item-dropdown text="Lang" right>
            <b-dropdown-item
              href="#"
              :value="lang"
              @click="
                lang = languages[0].name;
                sendMessage;
                langId = 0;
              "
              >{{ languages[0].name }}</b-dropdown-item
            >
            <b-dropdown-item
              href="#"
              :value="lang"
              @click="
                lang = languages[1].name;
                sendMessage;
                langId = 1;
              "
              >{{ languages[1].name }}</b-dropdown-item
            >
            <b-dropdown-item
              href="#"
              :value="lang"
              @click="
                lang = languages[2].name;
                sendMessage;
                langId = 2;
              "
              >{{ languages[2].name }}</b-dropdown-item
            >
          </b-nav-item-dropdown>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
</template>

<script>
export default {
  data() {
    return {
      languages: [
        {
          id: "0",
          name: "EN",
        },
        {
          id: "1",
          name: "ES",
        },
        {
          id: "2",
          name: "CAT",
        },
      ],
      lang: "",
      langId: "0",
      data: [
        {
          id: "0",
          lang: "english",
          elements: [
            {
              el1: "Home",
              el2: "About",
              el3: "Skills",
              el4: "Projects",
              el5: "Contact",
            },
          ],
        },
        {
          id: "1",
          lang: "español",
          elements: [
            {
              el1: "Inicio",
              el2: "Sobre mí",
              el3: "Habilidades",
              el4: "Proyectos",
              el5: "Contacto",
            },
          ],
        },
        {
          id: "2",
          lang: "català",
          elements: [
            {
              el1: "Inici",
              el2: "Sobre mí",
              el3: "Habilitats",
              el4: "Projectes",
              el5: "Contacte",
            },
          ],
        },
      ],
    };
  },
  methods: {},
};
</script>
<style lang="scss" scoped>
#nav a.nav-link {
  color: #fffffe;
}
#nav a.nav-link:hover {
  color: #ffc0ad;
}

#nav a.router-link-exact-active {
  color: #e68a6e;
}

img {
  height: 8vh;
}

b-navbar {
  background-color: black;
}
</style>
