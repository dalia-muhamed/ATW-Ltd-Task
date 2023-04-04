<template>
  <!-- <navbar :page="pages[activePage]"></navbar> -->
  <dynamic-links
    :pages="pages"
    :active-page="activePage"
    :nav-link-click="index => (activePage = index)"
  >
  </dynamic-links>
  <page-content :page="pages[activePage]"> </page-content>
</template>

<script>
import PageContent from './components/page-content/PageContent.vue';
import DynamicLinks from './components/dynamic-links/dynamicLinks.vue';
import Navbar from './components/navbar/Navbar.vue';

export default {
  components: {
    PageContent,
    DynamicLinks,
    // Navbar,
  },
  data() {
    return {
      activePage: 0,
      pages: [
        {
          link: { text: 'Home', url: 'index.html' },
          pageTitle: 'Home Page',
          content: 'this is home page content',
        },
        {
          link: { text: 'About', url: 'about.html' },
          pageTitle: 'About Page',
          content: 'this is about page content',
        },
        {
          link: { text: 'Project', url: 'projects.html' },
          pageTitle: 'Projects Page',
          content: 'this is Projects page content',
        },
        {
          link: { text: 'Contact', url: 'contact.html' },
          pageTitle: 'Contact Page',
          content: 'this is contact page content',
        },
      ],
      dynamicLinkPages: [
        {
          link: { text: 'web Design', url: 'web-design.html' },
          name: 'web Design',
        },
        {
          link: { text: 'Mobile App Design', url: 'mobile-app-design.html' },

          name: 'Mobile App Design',
        },
        {
          link: { text: 'Freebies', url: 'freebies.html' },

          name: 'Freebies',
        },
      ],
    };
  },
};
</script>
