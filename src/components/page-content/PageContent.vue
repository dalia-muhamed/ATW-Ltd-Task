<template>
  <div class="container">
    <!-- //TODO MAKE this list dynamic -->
    <!-- <li v-for="content in dynamicLinkPage.content"> -->
    <div class="media">
      <div class="img-container">
        <img class="img" src="../../assets/images/minify.svg" />
        <p class="img-title">Minify - Web Design</p>
        <div class="img-details">
          <p class="study-case">
            <img src="../../assets/icons/layers.svg" alt="layers icon" />View
            Study Case
          </p>
          <p class="live-preview">
            <img src="../../assets/icons/show.svg" alt="show icon" />Live
            Preview
          </p>
        </div>
      </div>
      <div class="img-container">
        <img class="img" src="../../assets/images/ant-personal.svg" />
        <p class="img-title">Ant - Personal Portofolio</p>
        <div class="img-details">
          <p class="study-case">
            <img src="../../assets/icons/layers.svg" alt="layers icon" />View
            Study Case
          </p>
          <p class="live-preview">
            <img src="../../assets/icons/show.svg" alt="show icon" />Live
            Preview
          </p>
        </div>
      </div>
      <div class="img-container">
        <img class="img" src="../../assets/images/lumy.svg" />
        <p class="img-title">Lumy - Dashboard UI Kit</p>
        <div class="img-details">
          <p class="study-case">
            <img src="../../assets/icons/layers.svg" alt="layers icon" />View
            Study Case
          </p>
          <p class="live-preview">
            <img src="../../assets/icons/show.svg" alt="show icon" />Live
            Preview
          </p>
        </div>
      </div>
      <div class="img-container">
        <img class="img" src="../../assets/images/keeper.svg" />
        <p class="img-title">Keeper - Soccer Site</p>
        <div class="img-details">
          <p class="study-case">
            <img src="../../assets/icons/layers.svg" alt="layers icon" />View
            Study Case
          </p>
          <p class="live-preview">
            <img src="../../assets/icons/show.svg" alt="show icon" />Live
            Preview
          </p>
        </div>
      </div>
      <!-- </li> -->
    </div>
  </div>
</template>

<script>
export default {
  props: ['dynamicLinkPage'],
  methods: {
    getImageSrc(imageName) {
      return `../../assets/${imageName}`;
    },
  },
};
</script>
