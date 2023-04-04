<template>
  <nav :class="`dynamic-links`">
    <div class="container-fluid">
      <ul class="navbar-nav">
        <li v-for="(page, index) in pages" class="nav-item" :key="index">
          <dynamic-links-link
            :page="page"
            :isActive="activePage === index"
            @click.prevent="navLinkClick(index)"
          ></dynamic-links-link>
        </li>
      </ul>
    </div>
  </nav>
</template>
<script>
import DynamicLinksLink from './dynamicLinksLink.vue';
export default {
  components: { DynamicLinksLink },
  props: ['pages', 'activePage', 'navLinkClick'],
};
</script>
<style>
.emphasize {
  border-bottom: 3px solid rgb(244, 210, 17);
}
</style>
