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
          url: 'web-design.html',
          content: 'welcome to web Design',
          name: 'Web Design',
        },
        {
          url: 'mobile-app-design.html',
          name: 'Mobile App Design',
          content: 'welcome to Mobile App Design',
        },
        {
          url: 'freebies.html',
          content: 'welcome to Freebies',
          name: 'Freebies',
        },
      ],
    };
  },
};
</script>
