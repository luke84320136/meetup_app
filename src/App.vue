<template>
  <v-app dark>
    <v-navigation-drawer temporary app fixed v-model="sideNav">
      <v-list>
        <v-list-tile>
          <v-list-tile-action>
            <v-icon>supervisor_account</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            View Meetups
          </v-list-tile-content>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>
    <v-toolbar app fixed class="error">
      <v-toolbar-side-icon @click.native.stop="sideNav = !sideNav" class="hidden-sm-and-up"></v-toolbar-side-icon>
      <v-toolbar-title>Meet Up</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-toolbar-items class="hidden-xs-only">
        <v-btn flat>
          <v-icon left>supervisor_account</v-icon>
          View meetups</v-btn>
      </v-toolbar-items>
    </v-toolbar>
    <v-footer app fixed>
      <span>&copy; 2018 LukeLan</span>
    </v-footer>
  </v-app>
</template>

<script>
  export default {
    data() {
      return {
        sideNav: false
      }
    }
  }
</script>