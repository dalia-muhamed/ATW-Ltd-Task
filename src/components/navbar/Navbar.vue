<template>
  <nav class="navbar">
    <div>
      <a class="navbar-brand" href="#">LOGO</a>
    </div>
    <ul class="navbar-nav">
      <li v-for="(page, index) in pages" class="nav-item" :key="index">
        <navbar-link :page="page"></navbar-link>
      </li>
    </ul>
  </nav>
  <header class="header">Our <br />Projects</header>
</template>

<script>
import NavbarLink from './NavbarLink.vue';

export default {
  components: { NavbarLink },
  props: ['pages'],
};
</script>
