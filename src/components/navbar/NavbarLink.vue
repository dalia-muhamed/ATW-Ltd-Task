<template>
  <a
    :href="page.url"
    class="nav-link"
    :class="activeClasses"
    :title="`this link goes to the ${page.text}page`"
    >{{ page.text }}
  </a>
</template>
<script>
export default {
  props: ['page', 'isActive'],
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
