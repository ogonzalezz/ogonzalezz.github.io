<template>
  <div class="fixed-top">
    <b-navbar toggleable="lg" type="dark">
      <b-navbar-brand href="#">
        <img src="../assets/logo3.svg" alt="Kitten" />
      </b-navbar-brand>

      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav>
          <b-nav-item to="/#homeSection">Home</b-nav-item>
          <b-nav-item to="/#aboutSection">About</b-nav-item>
          <b-nav-item to="/#skillsSection">Skills</b-nav-item>
          <b-nav-item to="/#ProjectsSection">Projects</b-nav-item>
          <b-nav-item to="/#contactSection">Contact</b-nav-item>
        </b-navbar-nav>

        <!-- Right aligned nav items -->
        <b-navbar-nav class="ml-auto">
          <b-nav-item-dropdown text="Lang" right>
            <b-dropdown-item href="#">EN</b-dropdown-item>
            <b-dropdown-item href="#">ES</b-dropdown-item>
            <b-dropdown-item href="#">CAT</b-dropdown-item>
          </b-nav-item-dropdown>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
</template>

<script>
export default {};
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
