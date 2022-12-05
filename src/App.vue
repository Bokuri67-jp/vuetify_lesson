<template>
  <v-app>
    <v-navigation-drawer app v-model="drawer" clipped>
      <v-container>
        <v-list-item>
          <v-list-item-content>
            <v-list-item-title class="title grey--text text--darken-2">
              Navigation Lists
            </v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-divider></v-divider>
        <v-list nav dense>
          <v-list-group
            v-for="nav_list in nav_lists"
            :key="nav_list.name"
            :prepend-icon="nav_list.icon"
            no-action
            :append-icon="nav_list.lists ? undefined : ''">
            <template v-slot:activator>
              <v-list-item-content>
                <v-list-item-title>{{nav_list.name}}</v-list-item-title>
              </v-list-item-content>
            </template>
            <v-list-item v-for="list in nav_list.lists" :key="list.name" :to="list.link">
              <v-list-item-contents>
                  <v-list-item-title>{{list.name}}</v-list-item-title>
              </v-list-item-contents>
            </v-list-item>
          </v-list-group>
        </v-list>
      </v-container>
    </v-navigation-drawer>

    <v-app-bar color="primary" dark app clipped-left>
      <v-app-bar-nav-icon @click="drawer=!drawer"></v-app-bar-nav-icon>
      <v-toolbar-title>Vuetify</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-toolbar-items>
        <v-btn text to="/enterprise">For Enterprise</v-btn>
        <v-menu offset-y>
          <template v-slot:activator="{on}">
            <v-btn text v-on="on">Support<v-icon>mdi-menu-down</v-icon></v-btn>
          </template>

          <v-list>
            <v-subheader>Get help</v-subheader>
            <v-list-item v-for="support in supports" :key="support.name" :to="support.link">
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
      <router-view />
    </v-main>

    <v-footer color="primary" dark app>
      Vuetify
    </v-footer>
</v-app>
</template>

<script>
// import SaleGraph from './components/SaleGraph'

export default {
  // components: { SaleGraph },
  data () {
    return {
      drawer: null,
      headers: [
        {
          text: 'Dessert (100g serving)',
          align: 'start',
          sortable: false,
          value: 'name'
        },
        { text: 'Calories', value: 'calories' },
        { text: 'Fat (g)', value: 'fat' },
        { text: 'Carbs (g)', value: 'carbs' },
        { text: 'Protein (g)', value: 'protein' },
        { text: 'Iron (%)', value: 'iron' }
      ],
      supports: [
        {
          name: 'Consulting and support',
          icon: 'mdi-vuetify',
          link: '/consulting-and-support'
        },
        {
          name: 'Discord community',
          icon: 'mdi-controller',
          link: '/discord-community'
        },
        {
          name: 'Report a bug',
          icon: 'mdi-bug',
          link: '/report-a-bug'
        },
        {
          name: 'Github issue board',
          icon: 'mdi-github',
          link: '/github-issue-board'
        },
        {
          name: 'Stack overview',
          icon: 'mdi-stack-overflow',
          link: '/stack-overview'
        }
      ],
      nav_lists: [
        {
          name: 'Resume',
          icon: '',
          lists: [
            {
              name: 'ResumeTable',
              link: '/ResumeTable'
            }
          ]
        },
        {
          name: 'Getting Started',
          icon: 'mdi-vuetify',
          lists: [
            {
              name: 'Quick Start',
              link: '/quick-start'
            },
            {
              name: 'Pre-mode layouts',
              link: '/pre-mode-layouts'
            }
          ]
        },
        {
          name: 'Customization',
          icon: 'mdi-cogs',
          link: '/customization'
        },
        {
          name: 'Styles & animations',
          icon: 'mdi-palette',
          lists: [
            {
              name: 'Colors',
              link: '/colors'
            },
            {
              name: 'Content',
              link: '/content'
            },
            {
              name: 'Display',
              link: '/display'
            }
          ]
        },
        {
          name: 'UI Components',
          icon: 'mdi-view-dashboard',
          lists: [
            {
              name: 'API explorer',
              link: '/api-explorer'
            },
            {
              name: 'Alerts',
              link: '/alerts'
            },
            {
              name: 'SaleGraph',
              link: '/salegraph'
            }
          ]
        },
        {
          name: 'Directives',
          icon: 'mdi-function',
          link: '/directives'
        },
        {
          name: 'Premium themes',
          icon: 'mdi-vuetify',
          link: '/premium-themes'
        },
        {
          name: 'Table',
          icon: 'mdi-file-table',
          lists: [
            {
              name: 'Desserts',
              link: '/desserts'
            }
          ]
        }
      ]
    }
  }
}

</script>
