<template>
  <nav>
    <HambugerMenuIcon @toggle="toggleMenu" class="nav-icon" />
    <div class="main-nav" v-show="menuVisible">
      <div class="content-nav">
        <ul>
          <li><a href="#">Catalogue</a></li>
          <li><a href="#">Ressources</a></li>
          <li><a href="#">FAQ</a></li>
          <li><a href="#">À propos</a></li>
        </ul>
        <div class="cta-header">
          <a href="#" class="cta-primary">Nous contacter</a>
        </div>
      </div>
    </div>
  </nav>
</template>

<script>
import HambugerMenuIcon from "./HamburgerMenuIcon.vue";

export default {
  components: {
    HambugerMenuIcon,
  },
  data() {
    return {
      menuVisible: false,
    };
  },
  methods: {
    toggleMenu() {
      this.menuVisible = !this.menuVisible;
    },
  },
};
</script>

<style>
.nav-icon {
  z-index: 1;
}
.content-nav {
  padding: 3rem;
}
.content-nav ul {
  list-style: none;
  padding: 0;
  margin: 0;
}
.content-nav ul li {
  margin-bottom: 2rem;
}
.content-nav ul li a {
  font-size: 2rem;
  text-decoration: none;
}
.main-nav {
  position: absolute;
  display: flex;
  align-items: flex-end;
  background-color: #fff;
  top: 0;
  right: 0;
  height: 100vh;
  width: 100vw;
}
</style>
