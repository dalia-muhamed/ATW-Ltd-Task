<template>
  <div class="container">
    <h1>{{ dynamicLinkPage.name }}</h1>
    <p>{{ dynamicLinkPage.content }}</p>
  </div>
</template>

<script>
export default {
  props: ['dynamicLinkPage'],
};
</script>
