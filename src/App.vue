<template>
  <v-app>
    <v-navigation-drawer app v-model="drawer" clipped>Navigation Lists</v-navigation-drawer>
    <v-app-bar color="primary" dark app clipped-left>
      <v-app-bar-nav-icon @click="drawer=!drawer"></v-app-bar-nav-icon>
      <v-toolbar-title>Vuetify</v-toolbar-title>
      <!-- <v-spacer></v-spacer> -->
      <v-toolbar-items>
        <v-btn text>For Enterprise</v-btn>
        <v-menu offset-y>
          <template v-slot:activator="{on}">
            <v-btn text v-on="on">Support<v-icon>mdi-menu-down</v-icon></v-btn>
          </template>
          <!-- <v-list>
            <v-list-item>
              <v-list-item-content>
                <v-list-item-title>Consulting and support</v-list-item-title>
              </v-list-item-content>
            </v-list-item>
            <v-list-item>
              <v-list-item-content>
                <v-list-item-title>Discord community</v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </v-list> -->
          <v-list>
            <v-subheader>Get help</v-subheader>
            <v-list-item v-for="support in supports" :key="support.name">
              <v-list-item-content>
                <v-list-item-title>
                  <v-list-item-icon>
                    <v-icon>{{support.icon}}</v-icon>
                  </v-list-item-icon>
                  {{support.name}}
                </v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </v-list>
        </v-menu>
      </v-toolbar-items>
    </v-app-bar>
    <v-main>
    </v-main>
    <v-footer color="primary" dark app>
      Vuetify
    </v-footer>
  </v-app>
</template>

<script>

export default {
  data () {
    return {
      drawer: null,
      supports: [
        { name: 'Consulting and support', icon: 'mdi-vuetify' },
        { name: 'Discord community', icon: 'mdi-controller' },
        { name: 'Report a bug', icon: 'mdi-bug' },
        { name: 'Github issue board', icon: 'mdi-github' },
        { name: 'Stack overview', icon: 'mdi-stack-overflow' }
      ]
    }
  }
}
</script>
