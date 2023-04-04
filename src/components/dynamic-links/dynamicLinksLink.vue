<template>
  <a
    :href="dynamicLinkPage.url"
    class="nav-link"
    :class="activeClasses"
    :title="`this link goes to the ${dynamicLinkPage.name}page`"
    >{{ dynamicLinkPage.name }}
  </a>
</template>
<script>
export default {
  props: ['dynamicLinkPage', 'isActive'],
  computed: {
    activeClasses() {
      return {
        active: this.isActive,
        emphasize: this.isActive,
      };
    },
  },
};
</script>
