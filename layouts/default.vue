<template>
  <v-app>    
    <img :src="'https://dummyimage.com/600x400/000/fff'">    
    <v-content>
      <v-container>
        <nuxt />
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Inspire',
          to: '/inspire'
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      tempTitle: 'XYZ'
    }
  },
  computed: {
    sharedContent: function() {
      return this.$store.state.agilityState.sharedContent
    },
    agilityPage: function() {
      return this.$store.state.agilityState.page
    },
    pageInSitemap: function() {
      return this.$store.state.agilityState.pageInSitemap
    },
    sitemapNested: function() {
      return this.$store.state.agilityState.sitemapNested
    }
  }
}
</script>
