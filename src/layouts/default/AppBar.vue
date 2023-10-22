<template>
  <v-app-bar color="pink">
    <v-app-bar-title>
      <v-icon icon="mdi-silverware" />
      &nbsp;&nbsp;
      My Pocket Menu
    </v-app-bar-title>
    <v-spacer />
    <v-btn @click="checkRoute('/')" icon to="/" :active="currentRoute == '/'">
      <v-icon icon="mdi-home"></v-icon>
    </v-btn>
    <v-btn @click="checkRoute('/settings')" icon to="/settings" :active="currentRoute == '/settings'">
      <v-icon icon="mdi-cogs"></v-icon>
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
    checkRoute: function (route) {
      this.currentRoute = route;
    }
  },
  mounted() {
    this.currentRoute = '/';
  }
}
</script>
