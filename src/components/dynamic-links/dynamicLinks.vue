<template>
  <nav :class="`dynamic-links`">
    <div class="container-fluid">
      <ul class="navbar-nav">
        <li
          v-for="(dynamicLinkPage, index) in dynamicLinkPages"
          class="nav-item"
          :key="index"
        >
          <dynamic-links-link
            :dynamicLinkPage="dynamicLinkPage"
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
  props: ['dynamicLinkPages', 'activePage', 'navLinkClick'],
};
</script>
<style>
.emphasize {
  border-bottom: 3px solid rgb(244, 210, 17);
}
</style>
