<template>
  <nav :class="`navbar`">
    <div class="container-fluid">
      <ul class="navbar-nav">
        <li v-for="(page, index) in pages" class="nav-item" :key="index">
          <navbar-link :page="page"></navbar-link>
        </li>
      </ul>
    </div>
  </nav>
</template>

<script>
import NavbarLink from './NavbarLink.vue';

export default {
  components: { NavbarLink },
  props: ['pages'],
};
</script>
