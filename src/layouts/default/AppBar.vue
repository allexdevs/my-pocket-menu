<template>
  <v-app-bar color="pink">
    <v-app-bar-title>
      <v-icon icon="mdi-silverware" />
      &nbsp;&nbsp;
      My Pocket Menu
    </v-app-bar-title>
    <v-spacer />
    <v-btn @click="getCurrentRoute" icon to="/" :active="currentRoute === '/'">
      <v-icon icon="mdi-home"></v-icon>
    </v-btn>
    <v-btn @click="getCurrentRoute" icon to="/settings" :active="currentRoute === '/settings'">
      <v-icon icon="mdi-file-document-plus"></v-icon>
    </v-btn>
  </v-app-bar>
</template>

<script>
export default {
  name: "AppBar",
  data() {
    return {
      currentRoute: ""
    }
  },
  methods: {
    getCurrentRoute: function () {
      setInterval(() => {
        this.currentRoute = this.$route.fullPath;
        console.log(this.currentRoute);
      }, 500);
    }
  },
  mounted() {
    this.getCurrentRoute();
  }
}
</script>
