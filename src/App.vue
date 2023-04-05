<template>
  <navbar :pages="pages"></navbar>
  <dynamic-links
    :dynamicLinkPages="dynamicLinkPages"
    :active-page="activePage"
    :nav-link-click="index => (activePage = index)"
  >
  </dynamic-links>
  <page-content :dynamicLinkPage="dynamicLinkPages[activePage]"> </page-content>
</template>

<script>
import PageContent from './components/page-content/PageContent.vue';
import DynamicLinks from './components/dynamic-links/dynamicLinks.vue';
import Navbar from './components/navbar/Navbar.vue';

export default {
  components: {
    PageContent,
    DynamicLinks,
    Navbar,
  },
  data() {
    return {
      activePage: 0,
      pages: [
        {
          text: 'Home',
          url: 'index.html',
        },
        {
          text: 'About',
          url: 'about.html',
        },
        {
          text: 'Project',
          url: 'projects.html',
        },
        {
          text: 'Contact',
          url: 'contact.html',
        },
      ],
      dynamicLinkPages: [
        {
          name: 'Web Design',
          url: 'web-design.html',
          content: ['minify.svg', 'lumy.svg', 'keeper.svg', 'ant-personal.svg'],
        },
        {
          name: 'Mobile App Design',
          url: 'mobile-app-design.html',
          content: ['minify.svg', 'lumy.svg'],
        },
        {
          name: 'Freebies',
          url: 'freebies.html',
          content: ['ant-personal.svg'],
        },
      ],
    };
  },
};
</script>
<style>
@font-face {
  font-family: Poppins;
  src: url('../src/assets/fonts/Poppins-SemiBold.ttf') format('truetype');
}
@font-face {
  font-family: PoppinsMedium;
  src: url('../src/assets/fonts/Poppins-Medium.ttf') format('truetype');
}
@font-face {
  font-family: extraPoppins;
  src: url('../src/assets/fonts/Poppins-Bold.ttf') format('truetype');
}
</style>
