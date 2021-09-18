<template>
  <nav
    class="w3-sidebar w3-collapse w3-white w3-animate-left"
    style="z-index:3;width:300px;"
    id="mySidebar"
  >
    <br />
    <div class="w3-container w3-row">
      <div class="w3-col s4">
        <img
          src="../assets/logo_mobisure.png"
          class="w3-circle w3-margin-right"
          style="width:46px"
        />
      </div>
      <div class="w3-col s8 w3-bar">
        <span>Bonjour, <strong>Mickaël</strong></span
        ><br />
        <a href="#" class="w3-bar-item w3-button"
          ><i class="fa fa-envelope"></i
        ></a>
        <a href="#" class="w3-bar-item w3-button"><i class="fa fa-user"></i></a>
        <a href="#" class="w3-bar-item w3-button"><i class="fa fa-cog"></i></a>
      </div>
    </div>
    <hr />
    <div class="w3-container">
      <h5>Tableau de bord</h5>
    </div>
    <div class="w3-bar-block">
      <a
        href="#"
        class="w3-bar-item w3-button w3-padding-16 w3-hide-large w3-dark-grey w3-hover-black"
        @click="closeMenu()"
        title="close menu"
        ><i class="fa fa-remove fa-fw"></i> Close Menu</a
      >
      <router-link class="w3-bar-item w3-button w3-padding" to="/"
        ><i class="fa fa-bank fa-fw"></i> Accueil</router-link
      >
      <router-link class="w3-bar-item w3-button w3-padding" to="/contact"
        ><i class="fa fa-pen fa-fw"></i> Contact</router-link
      >
    </div>
  </nav>
</template>

<script>
export default {
  name: "Nav",
  data() {
    return {
      SIDEBAR: ""
    };
  },
  methods: {
    closeMenu: function() {
      this.SIDEBAR.style.display = "none";
    }
  },
  mounted() {
    this.SIDEBAR = document.getElementById("mySidebar");
  }
};
</script>

<style scoped>
nav a.exact-active {
  background-color: rgb(8, 80, 80);
  color: white;
}
</style>
