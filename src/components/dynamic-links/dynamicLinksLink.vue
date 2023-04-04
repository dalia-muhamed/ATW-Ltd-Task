<template>
  <a
    :href="dynamicLinkPage.link.url"
    class="nav-link"
    :class="activeClasses"
    :title="`this link goes to the ${dynamicLinkPage.link.text}page`"
    >{{ dynamicLinkPage.link.text }}
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
