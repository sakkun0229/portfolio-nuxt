<template>
  <nav>
    <v-toolbar flat dark class="grey darken-4">
      <v-spacer></v-spacer>
      <v-toolbar-items class="hidden-xs-only">
        <v-btn text v-for="item in items" :key="item.title" :to="item.link" nuxt>
          <v-icon left>{{ item.icon }}</v-icon>
          {{ item.title }}
        </v-btn>
      </v-toolbar-items>
      <v-spacer></v-spacer>

      <v-toolbar-items class="d-sm-none">
        <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
      </v-toolbar-items>
    </v-toolbar>

    <v-navigation-drawer v-model="drawer" app right temporary class="grey darken-4">
      <v-list flat dark>
        <v-list-item v-for="item in items" :key="item.title" :to="item.link">
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      drawer: false,
      items: [
        { title: 'Home', icon: 'fas fa-home', link: '/' },
        { title: 'About', icon: 'fas fa-address-card', link: '/about' },
        { title: 'Skill', icon: 'fas fa-code', link: '/skill' },
        { title: 'Works', icon: 'fas fa-archive', link: '/works' },
        { title: 'Contact', icon: 'fas fa-envelope', link: '/contact' }
      ]
    }
  }
}
</script>
